---
title: Aggiunta di file a un processo
description: Un processo contiene uno o più file da trasferire.
ms.assetid: fb6e7219-b6ca-4f72-b7a3-60d65e8f3892
keywords:
- processo di trasferimento BITS , aggiunta di file
- trasferimento di file BITS , aggiunta
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: b6c369c0a9ee207790d0370da6543c642ee294b072e0d91f1837cd734a6a625d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529271"
---
# <a name="adding-files-to-a-job"></a>Aggiunta di file a un processo

Un processo contiene uno o più file da trasferire. Usare uno dei metodi seguenti per aggiungere file a un processo:

<dl> <dt>

<span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
</dt> <dd>

Aggiunge un singolo file a un processo.

</dd> <dt>

<span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
</dt> <dd>

Aggiunge uno o più file a un processo. Se si aggiungono più file, è più efficiente chiamare questo metodo anziché il **metodo AddFile** in un ciclo.

</dd> <dt>

<span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)
</dt> <dd>

Aggiunge un singolo file a un processo. Usare questo metodo se si vogliono scaricare intervalli di dati da un file. È possibile usare questo metodo solo per i processi di download.

</dd> </dl>

Quando si aggiunge un file a un processo, è necessario specificare il nome remoto e il nome locale del file. Per informazioni dettagliate sul formato dei nomi di file locali e remoti, vedere la [**struttura BG \_ FILE \_ INFO.**](/windows/desktop/api/Bits/ns-bits-bg_file_info)

Un processo di caricamento può contenere un solo file. I [**metodi IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) e [**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) restituiscono BG E TOO MANY FILES se si tenta di aggiungere più file a un processo di \_ \_ \_ \_ caricamento. Se è necessario caricare più di un file, è consigliabile usare un file CAB o ZIP.

Per i processi di download, BITS limita il numero di file che un utente può aggiungere a un processo a 200 file e il numero di intervalli per un file a 500 intervalli. Questi limiti non si applicano agli amministratori o ai servizi. Per modificare questi limiti predefiniti, vedere [Criteri di gruppo.](group-policies.md)

Il proprietario del processo o un utente con privilegi di amministratore può aggiungere file al processo in qualsiasi momento prima di chiamare il metodo [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o il metodo [**IBackgroundCopyJob::Cancel.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)

Se è necessario modificare il nome remoto del file dopo aver aggiunto il file al processo, è possibile chiamare il metodo [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) o il metodo [**IBackgroundCopyFile2::SetRemoteName.**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) Usare il **metodo ReplaceRemotePrefix** per modificare la parte del server del nome remoto quando il server non è disponibile o per consentire agli utenti in roaming di connettersi al server più vicino. Usare il **metodo SetRemoteName** per modificare il protocollo usato per trasferire il file o per modificare il nome o il percorso del file.

BITS crea un file temporaneo nella directory di destinazione e usa il file temporaneo per il trasferimento di file. Per ottenere il nome del file temporaneo, chiamare [**il metodo IBackgroundCopyFile3::GetTemporaryName.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) BITS modifica il nome del file temporaneo nel nome del file di destinazione quando si chiama il [**metodo**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Complete. BITS non specifica un descrittore [](/windows/desktop/api/fileapi/nf-fileapi-createfilea) di sicurezza quando crea il file temporaneo (il file eredita le informazioni ACL dalla directory di destinazione). Se i dati trasferiti sono sensibili, l'applicazione deve specificare un ACL appropriato nella directory di destinazione per impedire accessi non autorizzati.

Per mantenere le informazioni sul proprietario e sull'ACL con il file trasferito, chiamare il metodo [**IBackgroundCopyJob3::SetFileACLFlags.**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags)

Il proprietario del processo ( l'utente che [](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) ha creato il processo o l'amministratore che ha assunto la proprietà del processo) deve avere le autorizzazioni per il file sul server e sul client. Ad esempio, per scaricare un file, l'utente deve avere le autorizzazioni di lettura per il server e le autorizzazioni di scrittura per la directory locale nel client.

Nell'esempio seguente viene illustrato come aggiungere un singolo file al processo. Nell'esempio si presuppone che il puntatore a interfaccia [**IBackgroundCopyJob,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) pJob, sia valido.


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



Nell'esempio seguente viene illustrato come aggiungere più file al processo. Nell'esempio si presuppone che il puntatore di interfaccia [**IBackgroundCopyJob,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) pJob, sia valido e che i nomi locali e remoti provengono da un elenco nell'interfaccia utente.


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



 

 