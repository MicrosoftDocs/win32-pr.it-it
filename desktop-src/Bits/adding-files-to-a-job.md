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
# <a name="adding-files-to-a-job"></a><span data-ttu-id="b87b6-105">Aggiunta di file a un processo</span><span class="sxs-lookup"><span data-stu-id="b87b6-105">Adding Files to a Job</span></span>

<span data-ttu-id="b87b6-106">Un processo contiene uno o più file che si desidera trasferire.</span><span class="sxs-lookup"><span data-stu-id="b87b6-106">A job contains one or more files that you want to transfer.</span></span> <span data-ttu-id="b87b6-107">Per aggiungere file a un processo, usare uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b87b6-107">Use one of the following methods to add files to a job:</span></span>

<dl> <dt>

<span data-ttu-id="b87b6-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**Metodo ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span><span class="sxs-lookup"><span data-stu-id="b87b6-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span></span>
</dt> <dd>

<span data-ttu-id="b87b6-109">Aggiunge un singolo file a un processo.</span><span class="sxs-lookup"><span data-stu-id="b87b6-109">Adds a single file to a job.</span></span>

</dd> <dt>

<span data-ttu-id="b87b6-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**Metodo ibackgroundcopyjob:: AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span><span class="sxs-lookup"><span data-stu-id="b87b6-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span></span>
</dt> <dd>

<span data-ttu-id="b87b6-111">Aggiunge uno o più file a un processo.</span><span class="sxs-lookup"><span data-stu-id="b87b6-111">Adds one or more files to a job.</span></span> <span data-ttu-id="b87b6-112">Se si aggiungono più file, è più efficiente chiamare questo metodo anziché chiamare il metodo **AddFile** in un ciclo.</span><span class="sxs-lookup"><span data-stu-id="b87b6-112">If you are adding multiple files, it is more efficient to call this method than to call the **AddFile** method in a loop.</span></span>

</dd> <dt>

<span data-ttu-id="b87b6-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span><span class="sxs-lookup"><span data-stu-id="b87b6-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span></span>
</dt> <dd>

<span data-ttu-id="b87b6-114">Aggiunge un singolo file a un processo.</span><span class="sxs-lookup"><span data-stu-id="b87b6-114">Adds a single file to a job.</span></span> <span data-ttu-id="b87b6-115">Utilizzare questo metodo se si desidera scaricare gli intervalli di dati da un file.</span><span class="sxs-lookup"><span data-stu-id="b87b6-115">Use this method if you want to download ranges of data from a file.</span></span> <span data-ttu-id="b87b6-116">È possibile usare questo metodo solo per i processi di download.</span><span class="sxs-lookup"><span data-stu-id="b87b6-116">You can use this method only for download jobs.</span></span>

</dd> </dl>

<span data-ttu-id="b87b6-117">Quando si aggiunge un file a un processo, è necessario specificare il nome remoto e il nome locale del file.</span><span class="sxs-lookup"><span data-stu-id="b87b6-117">When you add a file to a job, you specify the remote name and the local name of the file.</span></span> <span data-ttu-id="b87b6-118">Per informazioni dettagliate sul formato dei nomi file locali e remoti, vedere la struttura di [**\_ \_ informazioni sul file BG**](/windows/desktop/api/Bits/ns-bits-bg_file_info) .</span><span class="sxs-lookup"><span data-stu-id="b87b6-118">For details on the format of the local and remote file names, see the [**BG\_FILE\_INFO**](/windows/desktop/api/Bits/ns-bits-bg_file_info) structure.</span></span>

<span data-ttu-id="b87b6-119">Un processo di caricamento può contenere un solo file.</span><span class="sxs-lookup"><span data-stu-id="b87b6-119">An upload job can contain only one file.</span></span> <span data-ttu-id="b87b6-120">I metodi [**Metodo ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) e [**Metodo ibackgroundcopyjob:: ADDFILESET**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) restituiscono BG \_ E \_ troppi \_ \_ file se si tenta di aggiungere più di un file a un processo di caricamento.</span><span class="sxs-lookup"><span data-stu-id="b87b6-120">The [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) and [**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) methods return BG\_E\_TOO\_MANY\_FILES if you try to add more than one file to an upload job.</span></span> <span data-ttu-id="b87b6-121">Se è necessario caricare più di un file, è consigliabile utilizzare un file CAB o ZIP.</span><span class="sxs-lookup"><span data-stu-id="b87b6-121">If you need to upload more than one file, consider using a CAB or ZIP file.</span></span>

<span data-ttu-id="b87b6-122">Per i processi di download, BITS limita il numero di file che un utente può aggiungere a un processo a 200 file e il numero di intervalli per un file a 500 intervalli.</span><span class="sxs-lookup"><span data-stu-id="b87b6-122">For download jobs, BITS limits the number of files that a user can add to a job to 200 files and the number of ranges for a file to 500 ranges.</span></span> <span data-ttu-id="b87b6-123">Questi limiti non si applicano agli amministratori o ai servizi.</span><span class="sxs-lookup"><span data-stu-id="b87b6-123">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="b87b6-124">Per modificare questi limiti predefiniti, vedere [criteri di gruppo](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b87b6-124">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="b87b6-125">Il proprietario del processo o un utente con privilegi di amministratore può aggiungere file al processo in qualsiasi momento prima di chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o il metodo [**Metodo ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="b87b6-125">The owner of the job or a user with administrator privileges can add files to the job anytime prior to calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>

<span data-ttu-id="b87b6-126">Se è necessario modificare il nome remoto del file dopo aver aggiunto il file al processo, è possibile chiamare il metodo [**IBackgroundCopyJob3:: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) o [**IBackgroundCopyFile2:: seremotename**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) .</span><span class="sxs-lookup"><span data-stu-id="b87b6-126">If you need to change the remote name of the file after you add the file to the job, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) method or the [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method.</span></span> <span data-ttu-id="b87b6-127">Utilizzare il metodo **ReplaceRemotePrefix** per modificare la porzione server del nome remoto quando il server non è disponibile o consentire agli utenti mobili di connettersi al server più vicino.</span><span class="sxs-lookup"><span data-stu-id="b87b6-127">Use the **ReplaceRemotePrefix** method to change the server portion of the remote name when the server is unavailable or to let roaming users connect to the closest server.</span></span> <span data-ttu-id="b87b6-128">Usare il metodo **Seremotename** per modificare il protocollo usato per trasferire il file o per modificare il nome o il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="b87b6-128">Use the **SetRemoteName** method to change the protocol used to transfer the file or to change the file name or path.</span></span>

<span data-ttu-id="b87b6-129">BITS crea un file temporaneo nella directory di destinazione e usa il file temporaneo per il trasferimento di file.</span><span class="sxs-lookup"><span data-stu-id="b87b6-129">BITS creates a temporary file in the destination directory and uses the temporary file for the file transfer.</span></span> <span data-ttu-id="b87b6-130">Per ottenere il nome del file temporaneo, chiamare il metodo [**IBackgroundCopyFile3:: Gettemporaryname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) .</span><span class="sxs-lookup"><span data-stu-id="b87b6-130">To get the temporary file name, call the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method.</span></span> <span data-ttu-id="b87b6-131">BITS modifica il nome del file temporaneo nel nome del file di destinazione quando si chiama il metodo [**complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="b87b6-131">BITS changes the temporary file name to the destination file name when you call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="b87b6-132">BITS non specifica un descrittore di sicurezza quando [**Crea**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) il file temporaneo (il file eredita le informazioni ACL dalla directory di destinazione).</span><span class="sxs-lookup"><span data-stu-id="b87b6-132">BITS does not specify a security descriptor when it [**creates**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) the temporary file (the file inherits the ACL information from the destination directory).</span></span> <span data-ttu-id="b87b6-133">Se i dati trasferiti sono sensibili, l'applicazione deve specificare un ACL appropriato nella directory di destinazione per impedire accessi non autorizzati.</span><span class="sxs-lookup"><span data-stu-id="b87b6-133">If the transferred data is sensitive, the application should specify an appropriate ACL on the destination directory to prevent unauthorized access.</span></span>

<span data-ttu-id="b87b6-134">Per mantenere le informazioni sul proprietario e sull'ACL con il file trasferito, chiamare il metodo [**IBackgroundCopyJob3:: SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) .</span><span class="sxs-lookup"><span data-stu-id="b87b6-134">To maintain the owner and ACL information with the transferred file, call the [**IBackgroundCopyJob3::SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) method.</span></span>

<span data-ttu-id="b87b6-135">Il proprietario del processo (l'utente che ha creato il processo o l'amministratore che [ha assunto la proprietà](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) del processo) deve disporre delle autorizzazioni per il file nel server e nel client.</span><span class="sxs-lookup"><span data-stu-id="b87b6-135">The owner of the job (the user who created the job or the administrator who [took ownership](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) of the job) must have permissions to the file on the server as well as the client.</span></span> <span data-ttu-id="b87b6-136">Per scaricare un file, ad esempio, l'utente deve disporre delle autorizzazioni di lettura sul server e delle autorizzazioni di scrittura per la directory locale nel client.</span><span class="sxs-lookup"><span data-stu-id="b87b6-136">For example, to download a file the user must have read permissions on the server and write permissions to the local directory on the client.</span></span>

<span data-ttu-id="b87b6-137">Nell'esempio seguente viene illustrato come aggiungere un singolo file al processo.</span><span class="sxs-lookup"><span data-stu-id="b87b6-137">The following example shows how to add a single file to the job.</span></span> <span data-ttu-id="b87b6-138">Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, sia valido.</span><span class="sxs-lookup"><span data-stu-id="b87b6-138">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid.</span></span>


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



<span data-ttu-id="b87b6-139">Nell'esempio seguente viene illustrato come aggiungere più file al processo.</span><span class="sxs-lookup"><span data-stu-id="b87b6-139">The following example shows how to add multiple files to the job.</span></span> <span data-ttu-id="b87b6-140">Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, sia valido e che i nomi locali e remoti provengano da un elenco nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b87b6-140">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid and the local and remote names come from a list in the user interface.</span></span>


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



 

 