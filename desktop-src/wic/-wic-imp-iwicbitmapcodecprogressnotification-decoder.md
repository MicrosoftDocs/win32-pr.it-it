---
description: Implementazione di IWICBitmapCodecProgressNotification (decodificatore)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implementazione di IWICBitmapCodecProgressNotification (decodificatore)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff9af6bbd8c0457a5bf97f2f8b378cdeaca9269e792f7ed4696ab8e6a23b89a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088063"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a>Implementazione di IWICBitmapCodecProgressNotification (decodificatore)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Quando un codec esegue un'operazione di I/O, ad esempio [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) su un'immagine di grandi dimensioni, il completamento potrebbe richiedere alcuni secondi o anche minuti. Quando gli utenti finali non sono in grado di interrompere un'operazione a esecuzione lunga, possono pensare che l'applicazione sia bloccata. Gli utenti spesso chiudono un'applicazione o addirittura riavviano i computer nel tentativo di riprendere il controllo del computer quando un'applicazione non risponde.

Questa interfaccia consente a un'applicazione di specificare una funzione di callback che il codec può chiamare a intervalli specificati per notificare al chiamante lo stato dell'operazione corrente. L'applicazione può usare questa funzione di callback per visualizzare un'indicazione dello stato di avanzamento nell'interfaccia utente per notificare all'utente lo stato dell'operazione. Se un utente fa clic sul **pulsante** Annulla nella **finestra** di dialogo Stato, l'applicazione restituisce **WINCODEC \_ ERR \_ ABORTED** dalla funzione di callback. In questo caso, il codec deve annullare l'operazione specificata e propagare questo **HRESULT** al chiamante del metodo che stava eseguendo l'operazione.

Questa interfaccia deve essere implementata nella classe del decodificatore a livello di contenitore.


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

Il *parametro pvData* punta a un oggetto che il chiamante vuole che il codec passi alla funzione di callback ogni volta che viene richiamata la funzione di callback. Questo oggetto può essere qualsiasi elemento e non ha alcun significato particolare per il codec.

Il *parametro dwProgressFlags* specifica quando il codec deve chiamare la funzione di callback. Una funzione OR può essere eseguita con due enumerazioni per questo parametro. L'enumerazione [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) specifica se chiamare la funzione di callback durante la decodifica (**WICProgressOperationCopyPixels),** la codifica (**WICProgerssOperationWritePixels**) o entrambe (**WICProgressOperationAll**).


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



Il codec deve chiamare la funzione di callback a intervalli regolari durante l'operazione, ma il chiamante può specificare determinati requisiti. [**L'enumerazione WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) indica a quale punto dell'operazione chiamare la funzione di callback. Se il chiamante specifica **WICProgressNotificationBegin,** è necessario chiamarlo all'inizio dell'operazione (0.0). Se il chiamante non lo specifica, è facoltativo. Analogamente, se il chiamante specifica **WICProgerssNotificationEnd,** è necessario chiamarlo al termine dell'operazione (1.0). Se il chiamante specifica **WICProgressNotificationAll,** è necessario chiamarlo all'inizio e alla fine, nonché a intervalli regolari durante l'operazione. Il chiamante può anche specificare **WICProgerssNotificationFrequent**, che indica che vuole essere richiamato a intervalli frequenti, ad esempio dopo ogni due righe di analisi. Un chiamante in genere userà questo flag solo per un'immagine molto grande. In caso contrario, in genere è consigliabile richiamare a intervalli di circa il 10% del numero totale di righe di analisi da elaborare.


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



È possibile registrare una sola funzione di callback alla volta per un decodificatore o un'istanza del codificatore specifica. Se un'applicazione chiama [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) più di una volta, sostituire la funzione di callback registrata in precedenza con quella nuova. Per annullare una registrazione di callback, un chiamante imposta il *parametro pfnProgressNotification* su **NULL.**

### <a name="pfnprogressnotification"></a>PFNProgressNotification

[**PFNProgressNotification è**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) la funzione di callback con la firma seguente.


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



Quando si richiama la funzione di callback, usare il *parametro pvData* per passare gli stessi *pvData* specificati dall'applicazione al momento della registrazione della funzione di callback.

Il *parametro uFrameNum* deve indicare l'indice del frame in corso di elaborazione.

Impostare il parametro operation su **WICProgressOperationCopyPixels** durante la decodifica e **WICProgressOperationWritePixels durante** la codifica.

Il *parametro dblProgress* deve essere un numero compreso tra 0,0 (inizio dell'operazione) e 1,0 (completamento dell'operazione). Il valore deve riflettere la percentuale di righe di analisi già elaborate rispetto al numero totale di righe di analisi da elaborare.

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

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



