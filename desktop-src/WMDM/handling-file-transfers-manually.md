---
title: Gestione manuale dei trasferimenti di file
description: Gestione manuale dei trasferimenti di file
ms.assetid: ff94191b-a0f2-4118-996c-d040f214fb9b
keywords:
- Windows Media Gestione dispositivi, trasferimenti di file manuali
- Gestione dispositivi, trasferimenti manuali di file
- Guida per programmatori, trasferimenti di file manuali
- applicazioni desktop, trasferimenti di file manuali
- creazione di applicazioni Windows Media Gestione dispositivi, trasferimenti manuali di file
- trasferimenti di file manuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bf12404e8cd83b6f0c0e4f1c8ec8b0b7bda205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728938"
---
# <a name="handling-file-transfers-manually"></a>Gestione manuale dei trasferimenti di file

L'applicazione può implementare l'interfaccia [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) per gestire parte del processo di lettura o scrittura. In una lettura dal dispositivo, l'implementazione consente all'applicazione di ricevere blocchi di dati non elaborati da un file del dispositivo. In una scrittura nel dispositivo, consente all'applicazione di inviare blocchi di dati non elaborati a un file nel dispositivo.

Nelle operazioni di lettura e scrittura il metodo [**IWMDMOperation:: TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) passa i dati tra il computer e il dispositivo. Per comprendere la direzione del trasferimento dei dati, l'applicazione deve impostare un flag quando Windows Media Gestione dispositivi chiama [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) o [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite). Quando viene chiamato il metodo [**end**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) , l'applicazione deve reimpostare questo flag.

> [!Note]  
> Se il provider di servizi e il dispositivo implementano correttamente [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2), verrà prima chiamato il metodo [IWMDMOperation3:: TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel) dell'applicazione, se implementato. Questo metodo rappresenta un modo più efficiente per trasferire i dati. **TransferObjectDataOnClearChannel** viene gestito allo stesso modo di **TransferObjectData**, ad eccezione del fatto che i dati non vengono mai crittografati e non sono presenti valori Mac da verificare.

 

Le sezioni seguenti descrivono sia il processo di lettura che quello di scrittura, quando l'applicazione implementa **IWMDMOperation**.

**Lettura da un dispositivo**

Quando si legge un file da un dispositivo, Windows Media Gestione dispositivi chiama i metodi **IWMDMOperation** seguenti nell'ordine indicato:

-   [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) Chiamato per notificare all'applicazione l'inizio di una lettura dal dispositivo.
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Chiamato una o più volte. L'elaborazione dei dati viene descritta nei passaggi seguenti:
    1.  **TransferObjectData** riceve un buffer, *pData*, di dimensioni *pdwSize* byte, compilato con dati e un Mac per verificare i dati in arrivo.
    2.  L'applicazione verifica i parametri in ingresso con il MAC dei dati in arrivo.
    3.  Tramite l'applicazione vengono decrittografati e letti tutti i dati in *pData* come possibile e viene modificato il valore restituito di *pdwSize* per indicare il numero di byte effettivamente letti.
    4.  L'applicazione decrittografa i dati, usando [**CSecureChannelClient::D ecryptparam**](/previous-versions/bb231586(v=vs.85))e li archivia o li usa, in base alle esigenze.
    5.  **TransferObjectData** restituisce \_ OK.
    6.  Windows Media Gestione dispositivi continua a chiamare **TransferObjectData** fino a quando l'applicazione non ha letto tutti i dati dal file o l'applicazione restituisce WMDM \_ E l' \_ utente \_ annullato per annullare l'operazione (nel qual caso la lettura viene annullata e Windows Media Gestione dispositivi chiama **end**).
-   [**Fine**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Chiamato per notificare all'applicazione che la lettura dal dispositivo sta per essere terminata.

**Scrittura in un dispositivo**

Quando si scrive un file nel dispositivo, Windows Media Gestione dispositivi chiama i metodi **IWMDMOperation** seguenti nell'ordine indicato:

-   [**GetObjectName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname) Chiamato per consentire all'applicazione di specificare un nome per la nuova risorsa di archiviazione. Questo metodo viene chiamato solo se l'applicazione non ha specificato un nome nel metodo **Insert** .
-   [**GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes) Chiamato per consentire all'applicazione di specificare gli attributi per la nuova risorsa di archiviazione nel dispositivo.
-   [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite) Chiamato per notificare l'inizio di una scrittura nel dispositivo.
-   [**GetObjectTotalSize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjecttotalsize) Chiamata eseguita per recuperare le dimensioni totali dell'oggetto scritto nel dispositivo, per consentire l'ottimizzazione del trasferimento e anche per concedere a Windows Media Gestione dispositivi la possibilità di annullare il trasferimento se il file è troppo grande per il dispositivo.
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Chiamato una o più volte. L'elaborazione dei dati viene descritta nei passaggi seguenti:
    1.  **TransferObjectData** riceve un puntatore a un buffer di dimensioni di *pdwSize* byte.
    2.  L'applicazione ottiene un blocco di dati da inviare al dispositivo, in genere leggendo i dati da un file e riempie il buffer ricevuto fino a *pdwSize* byte. Deve modificare *pdwSize* (se necessario) per riflettere il numero di byte aggiunti al buffer.
    3.  L'applicazione crea un MAC di tutti i parametri del metodo.
    4.  L'applicazione crittografa i dati nel buffer usando [**CSecureChannelClient:: EncryptParam**](/previous-versions/bb231587(v=vs.85)).
    5.  **TransferObjectData** restituisce \_ OK per indicare la presenza di più dati oppure s \_ false per indicare che non sono disponibili altri dati. Se l'applicazione restituisce WMDM \_ e \_ \_ l'utente è stato annullato, l'operazione di scrittura viene annullata e Windows Media Gestione dispositivi chiamerà **end**.
    6.  Windows Media Gestione dispositivi continua a chiamare **TransferObjectData** a condizione che l'applicazione restituisca S \_ OK.
-   [**Fine**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Chiamato per notificare la fine di una scrittura nel dispositivo.

Per un esempio di codice, vedere [crittografia e decrittografia](encryption-and-decryption.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un'applicazione Windows Media Gestione dispositivi**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 