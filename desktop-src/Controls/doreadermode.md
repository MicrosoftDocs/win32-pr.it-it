---
title: DoReaderMode (funzione)
description: Abilita la modalità lettore in una finestra.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- Controlli Windows per la funzione DoReaderMode
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
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479472"
---
# <a name="doreadermode-function"></a>DoReaderMode (funzione)

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

*prmi* \[ in\]
</dt> <dd>

Tipo: **PREADERMODEINFO**

Puntatore a una struttura [**READERMODEINFO**](readermodeinfo.md) contenente informazioni di inizializzazione per la modalità Reader.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La modalità lettore viene attivata tramite i dispositivi supportati con un clic del mouse, in genere utilizzando un terzo pulsante del mouse o una rotellina di scorrimento. Il successivo movimento del mouse in un'area specificata scorre il contenuto dell'area anziché spostare un puntatore. Al di fuori di tale area, il puntatore del mouse viene visualizzato e funziona normalmente. Un secondo clic del pulsante o della rotellina di scorrimento rilascia il dispositivo dalla modalità lettore.

> [!Note]  
> Questa funzione non è dichiarata in alcuna intestazione pubblica. Per usarlo, è necessario accedervi come ordinale 383 da Comctl32.dll.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, \[ solo app desktop di Windows Vista\]<br/>                                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 4,72 o successiva)</dt> </dl> |



 

 





