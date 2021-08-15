---
description: Ottiene il livello di una regola di identificazione hash che corrisponde all'hash specificato.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: Funzione SaferiSearchMatchingHashRules
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: c8b76d2bfbea8b106ea01d5ab4a939c1ebd33048eb5e4654c2a64746895c0df9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541481"
---
# <a name="saferisearchmatchinghashrules-function"></a>Funzione SaferiSearchMatchingHashRules

Ottiene il livello di una regola di identificazione hash che corrisponde all'hash specificato.

A questa funzione non è associata alcuna libreria di importazione e non viene dichiarata in un'intestazione pubblica. È necessario definire un puntatore a funzione con la firma di questa funzione ed è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico Advapi32.dll.

È consigliabile usare la [**funzione SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) per valutare i criteri di restrizione software.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HashAlgorithm* \[ in, facoltativo\]
</dt> <dd>

Identificatore dell'algoritmo utilizzato per creare l'hash.

</dd> <dt>

*pHashBytes* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di byte che contiene l'hash.

</dd> <dt>

*dwHashSize* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, della *matrice pHashBytes.*

</dd> <dt>

*dwOriginalImageSize* \[ in, facoltativo\]
</dt> <dd>

Dimensione, in byte, dell'immagine originale da cui è stato calcolato l'hash.

</dd> <dt>

*pdwFoundLevel* \[ Cambio\]
</dt> <dd>

Puntatore all'identificatore di livello per la regola di identificazione hash corrispondente.

</dd> <dt>

*pdwSaferFlags* 
</dt> <dd>

Riservato. Impostare questo valore su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TRUE** se la funzione ha esito positivo. in caso contrario, **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl> |



 

 
