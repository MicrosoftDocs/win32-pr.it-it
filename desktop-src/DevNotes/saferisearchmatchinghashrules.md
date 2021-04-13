---
description: Ottiene il livello di una regola di identificazione hash che corrisponde all'hash specificato.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: SaferiSearchMatchingHashRules (funzione)
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
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483645"
---
# <a name="saferisearchmatchinghashrules-function"></a>SaferiSearchMatchingHashRules (funzione)

Ottiene il livello di una regola di identificazione hash che corrisponde all'hash specificato.

Questa funzione non dispone di librerie di importazione associate e non è dichiarata in un'intestazione pubblica. È necessario definire un puntatore a funzione con la firma di questa funzione ed è necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Advapi32.dll.

È consigliabile usare la funzione [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) per valutare i criteri di restrizione software.

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

*pHashBytes* \[ in\]
</dt> <dd>

Puntatore a una matrice di byte che contiene l'hash.

</dd> <dt>

*dwHashSize* \[ in\]
</dt> <dd>

Dimensione, in byte, della matrice *pHashBytes* .

</dd> <dt>

*dwOriginalImageSize* \[ in, facoltativo\]
</dt> <dd>

Dimensione, in byte, dell'immagine originale da cui è stato calcolato l'hash.

</dd> <dt>

*pdwFoundLevel* \[ out\]
</dt> <dd>

Puntatore all'identificatore di livello per la regola di identificazione hash corrispondente.

</dd> <dt>

*pdwSaferFlags* 
</dt> <dd>

Riservato. Impostare questo valore su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**True** se la funzione ha esito positivo; in caso contrario, **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl> |



 

 
