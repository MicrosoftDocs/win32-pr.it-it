---
title: Funzione di callback ICMProgressProcCallback
description: La funzione ICMProgressProcCallback è una funzione di callback fornita dall'applicazione che segnala lo stato di avanzamento e consente all'applicazione di annullare l'elaborazione dei colori.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- Sistema di colori Windows per la funzione di callback ICMProgressProcCallback
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8acf790a135a41e4eabb4a67c2498f1ed914c4c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324347"
---
# <a name="icmprogressproccallback-callback-function"></a>Funzione di callback ICMProgressProcCallback

La funzione **ICMProgressProcCallback** è una funzione di callback fornita dall'applicazione che segnala lo stato di avanzamento e consente all'applicazione di annullare l'elaborazione dei colori.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulMax* 
</dt> <dd>

Specifica il valore massimo del contatore di stato (utilizzato per stimare il completamento dell'elaborazione della bitmap).

</dd> <dt>

*ulCurrent* 
</dt> <dd>

Specifica il valore corrente del contatore di stato (se diviso per il valore massimo, fornisce una stima approssimativa della percentuale di completamento).

</dd> <dt>

*ulCallbackData* 
</dt> <dd>

Specifica i dati passati dall'applicazione a una funzione ICM2, che quindi li passa alla funzione di callback. Tali dati possono essere utilizzati, ad esempio, per identificare la bitmap e il processo su cui viene segnalato lo stato di avanzamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** per continuare l'elaborazione di bitmap. Il valore restituito è **false** per annullare l'elaborazione. Se l'elaborazione viene annullata, la funzione chiamante restituisce zero per indicare un errore, anche se il buffer di output può essere riempito parzialmente.

## <a name="remarks"></a>Commenti

Il nome di questa funzione di callback viene fornito dall'applicazione. Diverse funzioni WCS, tra cui [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) e [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), chiamano questa funzione periodicamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>ICM. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Funzioni](functions.md)
</dt> <dt>

[**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
