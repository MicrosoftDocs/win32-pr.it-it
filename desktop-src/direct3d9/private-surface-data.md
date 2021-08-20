---
description: È possibile archiviare qualsiasi tipo di dati specifici dell'applicazione con una superficie. Ad esempio, una superficie che rappresenta una mappa in un gioco potrebbe contenere informazioni sul terreno.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Private Surface Data (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c010e24f691dc64c75e4dcea428af21d46ebfcb95b31775b9c8db81b2263e6d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520193"
---
# <a name="private-surface-data-direct3d-9"></a>Private Surface Data (Direct3D 9)

È possibile archiviare qualsiasi tipo di dati specifici dell'applicazione con una superficie. Ad esempio, una superficie che rappresenta una mappa in un gioco potrebbe contenere informazioni sul terreno.

Una superficie può avere più di un buffer di dati privato. Ogni buffer è identificato da un GUID fornito quando si collegano i dati alla superficie.

Per archiviare i dati della superficie privata, usare SetPrivateData, passando un puntatore al buffer di origine, le dimensioni dei dati e un GUID definito dall'applicazione per i dati. Facoltativamente, i dati di origine possono esistere sotto forma di oggetto COM. In questo caso, si passa un puntatore al puntatore di interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'oggetto e si imposta il flag D3DSPD \_ IUNKNOWNPOINTER.

SetPrivateData alloca un buffer interno per i dati e lo copia. È quindi possibile liberare in modo sicuro il buffer o l'oggetto di origine. Il riferimento interno al buffer o all'interfaccia viene rilasciato quando viene chiamato FreePrivateData. Questo avviene automaticamente quando la superficie viene liberata.

Per recuperare dati privati per una superficie, è necessario allocare un buffer delle dimensioni corrette e quindi chiamare il metodo GetPrivateData, passando il GUID assegnato ai dati. L'utente è responsabile di liberare qualsiasi memoria dinamica utilizzata per questo buffer. Se i dati sono un oggetto COM, questo metodo recupera il [**puntatore IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Se non si conosce la dimensione di un buffer da allocare, chiamare prima GetPrivateData con zero in pSizeOfData. Se il metodo ha esito negativo con D3DERR \_ MOREDATA, restituisce il numero di byte necessario per il buffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
