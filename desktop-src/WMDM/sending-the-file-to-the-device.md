---
title: Invio del file al dispositivo
description: Invio del file al dispositivo
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Windows Gestione dispositivi multimediali, invio di file ai dispositivi
- Gestione dispositivi, invio di file ai dispositivi
- guida alla programmazione, invio di file ai dispositivi
- applicazioni desktop, invio di file ai dispositivi
- creazione Windows applicazioni di Gestione dispositivi multimediali, invio di file ai dispositivi
- scrittura di file nei dispositivi, invio di file ai dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974a47de872d03d42701ff6e95516a9ead59f1206729ae9ca70d6dd9e5f1260f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124141"
---
# <a name="sending-the-file-to-the-device"></a>Invio del file al dispositivo

Dopo che il file è stato transcodificato se necessario ed è stato impostato tutti i metadati, incluso il formato, l'applicazione può inviare il file al dispositivo. A tale scopo, è necessario prima ottenere **un'interfaccia IWMDMStorageControl** (o una versione successiva) per un percorso di destinazione nel dispositivo. I **flag insert** specificano se la nuova archiviazione deve essere di pari livello o figlio della destinazione. Dopo aver ottenuto la destinazione, è possibile chiamare [**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)o [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) per trasferire il file. L'applicazione può gestire la lettura dei dati del file implementando [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)oppure può consentire al metodo **Insert** di leggere e trasferire automaticamente il file non fornendo un puntatore a un **oggetto IWMDMOperation implementato dall'applicazione.**

Il codice C++ seguente illustra la chiamata **di Insert3** per scrivere un file in un dispositivo. Se il *puntatore pOperation* passato a **Insert3** è **NULL,** il file verrà inviato in un unico passaggio. Se questo puntatore è un puntatore di interfaccia valido, Windows Gestione dispositivi multimediali chiamerà il metodo di callback per ottenere i dati in blocchi. Per informazioni dettagliate su come implementare **IWMDMOperation,** vedere [Gestione manuale dei trasferimenti di file.](handling-file-transfers-manually.md)


```C++
// Set the flags for the operation
UINT flags = WMDM_MODE_BLOCK | // Synchronous call. 
    WMDM_STORAGECONTROL_INSERTINTO | // Insert it into the destination folder.
    WMDM_CONTENT_FILE | // We're inserting a file.
    WMDM_FILE_CREATE_OVERWRITE; // Overwrite existing files.
if (pOperation != NULL)
    flags |= WMDM_CONTENT_OPERATIONINTERFACE;

// Send the file and metadata.
hr = pStgCtl3->Insert3(
    flags,
    WMDM_FILE_ATTR_FOLDER, // The current storage is a folder.
    const_cast<WCHAR*>(pwszFileName), // Source file.
    L"My New File.wma",//NULL, // Destination file name.
    pOperation, // NULL to allow the SDK to read the file; 
                // non-NULL to present raw data bytes to the SDK.
    pProgress, // Interface to send simple progress notifications.
    pMetadata, // IWMDMMetaData interface previously created and filled.
    NULL, 
    &pNewStorage); // Out: handle to the new storage, if the method succeeds.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file nel dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




