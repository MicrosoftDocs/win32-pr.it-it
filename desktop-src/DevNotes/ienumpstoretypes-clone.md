---
description: Crea un enumeratore aggiuntivo che contiene lo stesso stato di enumerazione di quello corrente.
ms.assetid: b4027520-62cc-40d4-b9fd-01fa9c652a54
title: 'Metodo IEnumPStoreTypes:: Clone (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4ac088ae708b62f458d7bba52127dadc8ef77c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332095"
---
# <a name="ienumpstoretypesclone-method"></a>Metodo IEnumPStoreTypes:: Clone

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Crea un enumeratore aggiuntivo che contiene lo stesso stato di enumerazione di quello corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Puntatore a un puntatore [**IEnumPStoreItems**](ienumpstoreitems.md) .

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

[**IEnumPStoreItems**](ienumpstoreitems.md)
</dt> <dt>

[**IEnumPStoreTypes**](ienumpstoretypes.md)
</dt> </dl>

 

 
