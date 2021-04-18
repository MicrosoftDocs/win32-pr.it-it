---
description: La funzione IsValidDevmode verifica che il contenuto di una struttura DEVMODE sia valido.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Funzione IsValidDevmode (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318372"
---
# <a name="isvaliddevmode-function"></a>IsValidDevmode (funzione)

La funzione **IsValidDevmode** verifica che il contenuto di una struttura DEVMODE sia valido.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevmode* \[ in\]
</dt> <dd>

Puntatore alla [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) da convalidare.

</dd> <dt>

*DevmodeSize* 
</dt> <dd>

Dimensioni in byte del buffer di byte di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**True** se l'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) è strutturalmente valido. Se vengono rilevati errori secondari, la funzione li correggerà e restituirà **true**.

**False** se [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) presenta uno o più problemi strutturali significativi. Il membro **dmSize** , ad esempio, non è allineato correttamente o specifica un buffer troppo piccolo. **False** anche se **pDevmode** è **null**.

## <a name="remarks"></a>Commenti

Non sono controllati campi di driver della stampante privati di [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , ma solo i campi pubblici.

I chiamanti devono usare **dmSize** + **dmDriverExtra** per **DevmodeSize** solo se possono garantire che la dimensione del buffer di input sia almeno quella grande. Poiché [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) è generalmente dati non attendibili, anche i valori presenti nel buffer di input in corrispondenza degli offset **dmSize** e **dmDriverExtra** non sono attendibili.

Questa funzione è eseguibile nel contesto di Least-Privileged account utente (LUA).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Winspool. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **IsValidDevmodeW** (Unicode) e **IsValidDevmodeA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




