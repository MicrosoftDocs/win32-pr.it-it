---
description: "Metodo IEnumPStoreTypes::Reset: reimposta all'inizio della sequenza di enumerazione."
ms.assetid: 35f14aa5-92cb-4ad8-b80c-2550dedb7a7f
title: Metodo IEnumPStoreTypes::Reset (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 55953a67d19ac94f792769974d860bae9b57f1ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089319"
---
# <a name="ienumpstoretypesreset-method"></a>Metodo IEnumPStoreTypes::Reset

\[L'archiviazione protetta (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Reimposta all'inizio della sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il valore restituito è **un valore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumPStoreTypes**](ienumpstoretypes.md)
</dt> </dl>

 

 
