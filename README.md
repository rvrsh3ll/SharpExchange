# ExchangeEmailDumper

This command line POC shows how C# can be used to interact with Microsoft Exchange. SHowing that it can be done in other tooling other than Powershell.
This is for educational purposes only. Dont use for evil or illegal things.

# Like the work dont forget to hit that Star Button and Sponsor

```
            
            Required Inputs (Must be in order shown):

            ReadEmailExchange.exe WEBDomain DomainName Password InternalDomainName DUMPItem
                Example WEBDomain: webmail.domain.com
                Example DomainName: User1
                Example Password: SecretPassword
                Example InternalDomainName: domain
                
                Options for DUMPItem:
                    Inbox
                    Sent
                    Drafts
                    Deleted
                    Skype
                    Attachments (Will Download Atatchments from the Inbox, DeletedItems, and Sent Items folders)
                    SendEmail ToEmailAddress~Subject~Body(Body can be file path)~AttachmentLocalFilePath(optional)
                    All (All == will try to dump all the items above)(I would default to this if unsure)

            Optional Inputs:

            ReadEmailExchange.exe WEBDomain DomainName Password InternalDomainName DUMPItem NumberOfSearchResultsToReturn
                            Example NumberOfSearchResultsToReturn (will return a maximum of the number,default 10): 10
                            Note: NumberOfSearchResultsToReturn must be a int/whole number

            Optional Inputs:

            ReadEmailExchange.exe WEBDomain DomainName Password InternalDomainName DUMPItem NumberOfSearchResultsToReturn OutputFileNameOrPath
                Example OutputFileNameOrPath: C:\file.csv
                Note: Program needs permission to write to location
                