---
title: Metodo IEnumFsiItems RemoteNext
description: Supporta un client remoto che desidera recuperare un numero specificato di elementi nella sequenza di enumerazione. | Metodo IEnumFsiItems RemoteNext
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- Metodo RemoteNext IMAPi
- Metodo RemoteNext IMAPi, interfaccia IEnumFsiItems
- Interfaccia IEnumFsiItems IMAPi, Metodo RemoteNext
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e29d3f75cd8e2f83fcd21236661d0d1fa0dabef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530714"
---
# <a name="ienumfsiitemsremotenext-method"></a>Metodo IEnumFsiItems:: RemoteNext

Supporta un client remoto che desidera recuperare un numero specificato di elementi nella sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ in\]
</dt> <dd>

Numero di elementi da recuperare.

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Matrice di interfacce [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) . Al termine, è necessario rilasciare ogni interfaccia in rgelt.

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Numero di elementi restituiti in rgelt. Se *celt* è uno, è possibile impostare *pceltFetched* su **null** . In caso contrario, inizializzare il valore di *pceltFetched* su 0 prima di chiamare questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

\_Viene restituito S OK quando il numero di elementi richiesti (*celt*) viene restituito correttamente o il numero di elementi restituiti (*pceltFetched*) è inferiore al numero di elementi richiesti.

Altri codici di riuscita possono essere restituiti come risultato dell'implementazione. I codici di errore seguenti vengono in genere restituiti in caso di errore dell'operazione, ma non rappresentano solo i possibili valori di errore:



| Codice restituito                                                                                   | Descrizione                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Puntatore non valido.<br/> Valore: 0x80004003<br/>                   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Impossibile allocare la memoria necessaria.<br/> Valore: 0x8007000E<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno o più argomenti non sono validi.<br/> Valore: 0x80070057<br/>    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, \[ solo app desktop Windows XP con SP2\]<br/>                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| IDL<br/>                      | <dl> <dt>Imapi2fs. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumFsiItems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[IEnumFsiItems:: Next](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 





