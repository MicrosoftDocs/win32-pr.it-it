---
description: Inviato a tutte le finestre di primo livello quando il sistema rileva più del 12,5% del tempo di sistema in un intervallo da 30 a 60 secondi, viene utilizzata la compattazione della memoria. Ciò indica che la memoria di sistema è insufficiente.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: WM_COMPACTING messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553662bccb223ed7fb987df5d2918e3d8d1c6ab95f125cbacbd50c1e2484c0c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200572"
---
# <a name="wm_compacting-message"></a>MESSAGGIO DI \_ COMPATTAZIONE WM

Inviato a tutte le finestre di primo livello quando il sistema rileva più del 12,5% del tempo di sistema in un intervallo da 30 a 60 secondi, viene utilizzata la compattazione della memoria. Ciò indica che la memoria di sistema è insufficiente.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> [!Note]  
> Questo messaggio viene fornito solo per la compatibilità con le applicazioni Windows a 16 bit.

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Rapporto tra il tempo dell'unità di elaborazione centrale (CPU) attualmente impiegato dal sistema che compatta la memoria e il tempo di CPU attualmente impiegato dal sistema che esegue altre operazioni. Ad esempio, 0x8000 rappresenta il 50% del tempo cpu impiegato per compattare la memoria.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Quando un'applicazione riceve questo messaggio, deve liberare la maggior quantità di memoria possibile, tenendo conto del livello corrente di attività dell'applicazione e del numero totale di applicazioni in esecuzione nel sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Panoramica](windows.md)
</dt> </dl>

 

 
