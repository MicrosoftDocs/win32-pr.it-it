---
description: Implementazione di IWICBitmapCodecProgressNotification (decodificatore)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implementazione di IWICBitmapCodecProgressNotification (decodificatore)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312970"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a>Implementazione di IWICBitmapCodecProgressNotification (decodificatore)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Quando un codec sta eseguendo un'operazione di I/O, ad esempio [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) su un'immagine di grandi dimensioni, il completamento potrebbe richiedere alcuni secondi o persino minuti. Quando gli utenti finali non sono in grado di interrompere un'operazione a esecuzione prolungata, potrebbero ritenere che l'applicazione sia bloccata. Spesso gli utenti chiudono un'applicazione o addirittura riavviano i computer, nel tentativo di riottenere il controllo del computer quando un'applicazione non risponde.

Questa interfaccia consente a un'applicazione di specificare una funzione di callback che il codec può chiamare a intervalli specificati per notificare al chiamante lo stato di avanzamento dell'operazione corrente. L'applicazione può utilizzare questa funzione di callback per visualizzare un'indicazione dello stato di avanzamento nell'interfaccia utente per notificare all'utente lo stato dell'operazione. Se un utente fa clic sul pulsante **Annulla** nella finestra di dialogo **stato** , l'applicazione restituisce **WINCODEC \_ Err \_ interrotto** dalla funzione di callback. Quando si verifica questo problema, il codec deve annullare l'operazione specificata e propagare questo **HRESULT** al chiamante del metodo che stava eseguendo l'operazione.

Questa interfaccia deve essere implementata nella classe decodificatore a livello di contenitore.


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [RegisterProgressNotification](#registerprogressnotification)
-   [PFNProgressNotification](#pfnprogressnotification)

### <a name="registerprogressnotification"></a>RegisterProgressNotification

[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) viene richiamato da un'applicazione per registrare una funzione di callback che il codec può chiamare a intervalli specificati. Il primo parametro, *pfnProgressNotification*, è un puntatore alla funzione di callback che il codec deve chiamare a intervalli regolari.

Il parametro *pvData* punta a un oggetto che il chiamante desidera che il codec passi di nuovo alla funzione di callback ogni volta che viene richiamata la funzione di callback. Questo oggetto può essere qualsiasi elemento e non ha un significato particolare per il codec.

Il parametro *dwProgressFlags* specifica quando il codec deve chiamare la funzione di callback. Una funzione OR può essere eseguita con due enumerazioni per questo parametro. L'enumerazione [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) specifica se chiamare la funzione di callback durante la decodifica (**WICProgressOperationCopyPixels**), la codifica (**WICProgerssOperationWritePixels**) o entrambe (**WICProgressOperationAll**).


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



Il codec deve chiamare la funzione di callback a intervalli regolari durante l'operazione, ma il chiamante può specificare determinati requisiti. L'enumerazione [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) indica in quale punto dell'operazione chiamare la funzione di callback. Se il chiamante specifica **WICProgressNotificationBegin**, è necessario chiamarlo all'inizio dell'operazione (0,0). Se il chiamante non specifica questo, è facoltativo. Analogamente, se il chiamante specifica **WICProgerssNotificationEnd**, è necessario chiamarlo al termine dell'operazione (1,0). Se il chiamante specifica **WICProgressNotificationAll**, è necessario chiamarlo all'inizio e alla fine, così come a intervalli regolari durante l'operazione. Il chiamante può inoltre specificare **WICProgerssNotificationFrequent**, che indica che si desidera richiamarli a intervalli frequenti, ad esempio dopo ogni paio di righe di analisi. Un chiamante utilizzerà in genere questo flag solo per un'immagine di grandi dimensioni. In caso contrario, è in genere necessario richiamare a intervalli di circa il 10% di incrementi del numero totale di righe di analisi da elaborare.


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



È possibile registrare una sola funzione di callback alla volta per un'istanza specifica del codificatore o del codificatore. Se un'applicazione chiama [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) più di una volta, sostituire la funzione di callback precedentemente registrata con quella nuova. Per annullare una registrazione di callback, un chiamante imposterà il parametro *pfnProgressNotification* su **null**.

### <a name="pfnprogressnotification"></a>PFNProgressNotification

[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) è la funzione di callback con la firma seguente.


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



Quando si richiama la funzione di callback, usare il parametro *pvData* per passare di nuovo lo stesso *pvData* specificato dall'applicazione al momento della registrazione della funzione di callback.

Il parametro *uFrameNum* deve indicare l'indice del frame in fase di elaborazione.

Impostare il parametro Operation su **WICProgressOperationCopyPixels** durante la decodifica e **WICProgressOperationWritePixels** durante la codifica.

Il parametro *dblProgress* deve essere un numero compreso tra 0,0 (inizio dell'operazione) e 1,0 (il completamento dell'operazione). Il valore deve riflettere la proporzione di righe di analisi già elaborate rispetto al numero totale di righe di analisi da elaborare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**ProgressNotificationCallback**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Implementazione di IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



