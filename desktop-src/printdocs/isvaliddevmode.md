---
description: La funzione IsValidDevmode verifica che il contenuto di una struttura DEVMODE sia valido.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Funzione IsValidDevmode (Winspool.h)
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
ms.openlocfilehash: 4c3a5cd33a6a5584ea9373df22df51a09e3e763d284a0f979f0b24e3651dc3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100529"
---
# <a name="isvaliddevmode-function"></a>Funzione IsValidDevmode

La **funzione IsValidDevmode** verifica che il contenuto di una struttura DEVMODE sia valido.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevmode* \[ Pollici\]
</dt> <dd>

Puntatore a [**DEVMODE da**](/windows/win32/api/wingdi/ns-wingdi-devmodea) convalidare.

</dd> <dt>

*DevmodeSize* 
</dt> <dd>

Dimensione in byte del buffer di byte di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TRUE** se [**DEVMODE è strutturalmente**](/windows/win32/api/wingdi/ns-wingdi-devmodea) valido. Se vengono rilevati errori secondari, la funzione li correggerà e restituirà **TRUE.**

**FALSE** se [**devMODE presenta**](/windows/win32/api/wingdi/ns-wingdi-devmodea) uno o più problemi strutturali significativi. Ad esempio, il **relativo membro dmSize** non è allineato o specifica un buffer troppo piccolo. False se **pDevmode è** **NULL.** 

## <a name="remarks"></a>Commenti

Non viene selezionato alcun campo del driver della stampante privato di [**DEVMODE,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) ma solo i campi pubblici.

I chiamanti devono **usare** + **dmSize dmDriverExtra** per **DevmodeSize** solo se possono garantire che le dimensioni del buffer di input siano almeno tali. Poiché [**devMODE è**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in genere dati non attendibili, anche i valori presenti nel buffer di input in corrispondenza degli offset **dmSize** e **dmDriverExtra** non sono attendibili.

Questa funzione è eseguibile in Least-Privileged contesto dell'account utente (LUA).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Winspool.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **IsValidDevmodeW** (Unicode) e **IsValidDevmodeA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




