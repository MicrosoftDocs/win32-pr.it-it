---
description: È possibile archiviare qualsiasi tipo di dati specifici dell'applicazione con una superficie. Una superficie che rappresenta una mappa in un gioco, ad esempio, potrebbe contenere informazioni sul terreno.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Dati della superficie privata (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304380"
---
# <a name="private-surface-data-direct3d-9"></a>Dati della superficie privata (Direct3D 9)

È possibile archiviare qualsiasi tipo di dati specifici dell'applicazione con una superficie. Una superficie che rappresenta una mappa in un gioco, ad esempio, potrebbe contenere informazioni sul terreno.

Una superficie può avere più di un buffer di dati privato. Ogni buffer viene identificato da un GUID fornito quando si alleghino i dati alla superficie.

Per archiviare i dati della superficie privata, utilizzare SetPrivateData, passando un puntatore al buffer di origine, la dimensione dei dati e un GUID definito dall'applicazione per i dati. Facoltativamente, i dati di origine possono esistere sotto forma di oggetto COM; in questo caso, si passa un puntatore al puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'oggetto e si imposta il \_ flag D3DSPD IUNKNOWNPOINTER.

SetPrivateData alloca un buffer interno per i dati e lo copia. È quindi possibile liberare in modo sicuro il buffer o l'oggetto di origine. Il buffer interno o il riferimento all'interfaccia viene rilasciato quando viene chiamato FreePrivateData. Questa operazione viene eseguita automaticamente quando viene liberata la superficie.

Per recuperare i dati privati per una superficie, è necessario allocare un buffer con la dimensione corretta, quindi chiamare il metodo GetPrivateData, passando il GUID assegnato ai dati. L'utente è responsabile di liberare la memoria dinamica usata per questo buffer. Se i dati sono un oggetto COM, questo metodo recupera il puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

Se non si conosce la dimensione di un buffer da allocare, chiamare prima GetPrivateData con zero in pSizeOfData. Se il metodo ha esito negativo con D3DERR \_ MOREDATA, restituisce il numero di byte necessari per il buffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
