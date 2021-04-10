---
title: Aggiunta di file a un processo
description: Un processo contiene uno o più file che si desidera trasferire.
ms.assetid: fb6e7219-b6ca-4f72-b7a3-60d65e8f3892
keywords:
- trasferimento di bit di processo, aggiunta di file
- BIT di trasferimento di file, aggiunta
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: ecb46a535fee117750b8b46066d798a4525aa44c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963226"
---
# <a name="adding-files-to-a-job"></a>Aggiunta di file a un processo

Un processo contiene uno o più file che si desidera trasferire. Per aggiungere file a un processo, usare uno dei metodi seguenti:

<dl> <dt>

<span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**Metodo ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
</dt> <dd>

Aggiunge un singolo file a un processo.

</dd> <dt>

<span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**Metodo ibackgroundcopyjob:: AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
</dt> <dd>

Aggiunge uno o più file a un processo. Se si aggiungono più file, è più efficiente chiamare questo metodo anziché chiamare il metodo **AddFile** in un ciclo.

</dd> <dt>

<span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)
</dt> <dd>

Aggiunge un singolo file a un processo. Utilizzare questo metodo se si desidera scaricare gli intervalli di dati da un file. È possibile usare questo metodo solo per i processi di download.

</dd> </dl>

Quando si aggiunge un file a un processo, è necessario specificare il nome remoto e il nome locale del file. Per informazioni dettagliate sul formato dei nomi file locali e remoti, vedere la struttura di [**\_ \_ informazioni sul file BG**](/windows/desktop/api/Bits/ns-bits-bg_file_info) .

Un processo di caricamento può contenere un solo file. I metodi [**Metodo ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) e [**Metodo ibackgroundcopyjob:: ADDFILESET**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) restituiscono BG \_ E \_ troppi \_ \_ file se si tenta di aggiungere più di un file a un processo di caricamento. Se è necessario caricare più di un file, è consigliabile utilizzare un file CAB o ZIP.

Per i processi di download, BITS limita il numero di file che un utente può aggiungere a un processo a 200 file e il numero di intervalli per un file a 500 intervalli. Questi limiti non si applicano agli amministratori o ai servizi. Per modificare questi limiti predefiniti, vedere [criteri di gruppo](group-policies.md).

Il proprietario del processo o un utente con privilegi di amministratore può aggiungere file al processo in qualsiasi momento prima di chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o il metodo [**Metodo ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .

Se è necessario modificare il nome remoto del file dopo aver aggiunto il file al processo, è possibile chiamare il metodo [**IBackgroundCopyJob3:: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) o [**IBackgroundCopyFile2:: seremotename**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) . Utilizzare il metodo **ReplaceRemotePrefix** per modificare la porzione server del nome remoto quando il server non è disponibile o consentire agli utenti mobili di connettersi al server più vicino. Usare il metodo **Seremotename** per modificare il protocollo usato per trasferire il file o per modificare il nome o il percorso del file.

BITS crea un file temporaneo nella directory di destinazione e usa il file temporaneo per il trasferimento di file. Per ottenere il nome del file temporaneo, chiamare il metodo [**IBackgroundCopyFile3:: Gettemporaryname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) . BITS modifica il nome del file temporaneo nel nome del file di destinazione quando si chiama il metodo [**complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . BITS non specifica un descrittore di sicurezza quando [**Crea**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) il file temporaneo (il file eredita le informazioni ACL dalla directory di destinazione). Se i dati trasferiti sono sensibili, l'applicazione deve specificare un ACL appropriato nella directory di destinazione per impedire accessi non autorizzati.

Per mantenere le informazioni sul proprietario e sull'ACL con il file trasferito, chiamare il metodo [**IBackgroundCopyJob3:: SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) .

Il proprietario del processo (l'utente che ha creato il processo o l'amministratore che [ha assunto la proprietà](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) del processo) deve disporre delle autorizzazioni per il file nel server e nel client. Per scaricare un file, ad esempio, l'utente deve disporre delle autorizzazioni di lettura sul server e delle autorizzazioni di scrittura per la directory locale nel client.

Nell'esempio seguente viene illustrato come aggiungere un singolo file al processo. Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, sia valido.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;

//Replace parameters with variables that contain valid paths.
hr = pJob->AddFile(L"https://ServerName/Path/File.Ext", L"d:\\Path\\File.Ext");
if (SUCCEEDED(hr))
{
  //Do something.
}
```



Nell'esempio seguente viene illustrato come aggiungere più file al processo. Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, sia valido e che i nomi locali e remoti provengano da un elenco nell'interfaccia utente.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_FILE_INFO* paFiles = NULL;
ULONG idx = 0;
ULONG nCount = 0;            //Set to the number of files to add to the job.
LPWSTR pszLocalName = NULL;  //Comes from the list in the user interface.
LPWSTR pszRemoteName = NULL; //Comes from the list in the user interface.

//Set nCount to the number of files to transfer.

//Allocate a block of memory to contain the array of BG_FILE_INFO structures.
//The BG_FILE_INFO structure contains the local and remote names of the 
//file being transferred.
paFiles = (BG_FILE_INFO*) malloc(sizeof(BG_FILE_INFO) * nCount);
if (NULL == paFiles)
{
  //Handle error
}
else
{
  //Add local and remote file name pairs to the memory block. 
  for (idx=0; idx<nCount; idx++)
  {
    //Set pszLocalName to point to an LPWSTR that contains the local name or
    //allocate memory for pszLocalName and copy the local name to pszLocalName.
    (paFiles+idx)->LocalName = pszLocalName;

    //Set pszRemoteName to point to an LPWSTR that contains the remote name or
    //allocate memory for pszRemoteName and copy the remote name to pszRemoteName.
    (paFiles+idx)->RemoteName = pszRemoteName;
  }

  //Add the files to the job.
  hr = pJob->AddFileSet(nCount, paFiles);
  if (SUCCEEDED(hr))
  {
     //Do Something.
  }

  //Free the memory block for the array of BG_FILE_INFO structures. If you allocated
  //memory for the local and remote file names, loop through the array and free the
  //memory for the file names before you free paFiles.
  free(paFiles);
}
```



 

 