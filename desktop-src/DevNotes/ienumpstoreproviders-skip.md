---
description: Ignora il numero specificato successivo di elementi nella sequenza di enumerazione.
ms.assetid: bf9ea700-3f44-48a7-8ea0-ee66dea61836
title: 'Metodo IEnumPStoreProviders:: Skip (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 75ec981e76d387f6ada82869bba40fa4946ce7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326207"
---
# <a name="ienumpstoreprovidersskip-method"></a>Metodo IEnumPStoreProviders:: Skip

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Ignora il numero specificato successivo di elementi nella sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ in\]
</dt> <dd>

Numero di tipi di provider da ignorare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
