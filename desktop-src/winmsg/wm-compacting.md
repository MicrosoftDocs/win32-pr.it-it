---
description: Inviato a tutte le finestre di primo livello quando il sistema rileva più del 12,5% del tempo di sistema in un intervallo da 30 a 60 secondi viene impiegato per la compattazione della memoria. Indica che la memoria di sistema è insufficiente.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: Messaggio WM_COMPACTING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314872"
---
# <a name="wm_compacting-message"></a>\_Messaggio di compattazione WM

Inviato a tutte le finestre di primo livello quando il sistema rileva più del 12,5% del tempo di sistema in un intervallo da 30 a 60 secondi viene impiegato per la compattazione della memoria. Indica che la memoria di sistema è insufficiente.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> Questo messaggio viene fornito solo per la compatibilità con le applicazioni basate su Windows a 16 bit.

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Rapporto tra il tempo di unità di elaborazione centrale (CPU) attualmente impiegato dal sistema per la compattazione della memoria e il tempo di CPU attualmente impiegato dal sistema per l'esecuzione di altre operazioni. Ad esempio, 0x8000 rappresenta il 50% del tempo di CPU dedicato alla compattazione della memoria.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Quando un'applicazione riceve questo messaggio, deve liberare il maggior numero di memoria possibile, prendendo in considerazione il livello corrente di attività dell'applicazione e il numero totale di applicazioni in esecuzione nel sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Windows](windows.md)
</dt> </dl>

 

 
