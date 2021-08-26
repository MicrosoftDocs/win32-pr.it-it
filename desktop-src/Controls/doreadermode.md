---
title: Funzione DoReaderMode
description: Abilita la modalità lettore in una finestra.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- Controlli Windows DoReaderMode
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63b71538e41e4b70155da8352e531b620fbe5de7f62746713c3a2a58f3adddf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002691"
---
# <a name="doreadermode-function"></a>Funzione DoReaderMode

\[**DoReaderMode** è disponibile tramite Windows XP con Service Pack 2 (SP2). Potrebbe non essere disponibile nelle versioni successive.\]

Abilita la modalità lettore in una finestra.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*prmi* \[ Pollici\]
</dt> <dd>

Tipo: **PREADERMODEINFO**

Puntatore a una struttura [**READERMODEINFO**](readermodeinfo.md) che contiene informazioni di inizializzazione per la modalità lettore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La modalità lettore viene attivata tramite dispositivi supportati tramite un clic del mouse, in genere usando un terzo pulsante del mouse o una rotellina di scorrimento. Lo spostamento successivo del mouse in un'area specificata scorre il contenuto dell'area anziché spostare un puntatore. All'esterno di tale area, il puntatore del mouse viene visualizzato e funziona normalmente. Un secondo clic del pulsante o della rotellina di scorrimento rilascia il dispositivo dalla modalità lettore.

> [!Note]  
> Questa funzione non è dichiarata in alcuna intestazione pubblica. Per usarlo, è necessario accedervi come ordinale 383 da Comctl32.dll.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows solo \[ app desktop di Vista\]<br/>                                                   |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 4.72 o successiva)</dt> </dl> |



 

 





