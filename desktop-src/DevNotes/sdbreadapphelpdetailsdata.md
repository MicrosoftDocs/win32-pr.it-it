---
Description: Recupera i dati dal database dettagli apphelp.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: SdbReadApphelpDetailsData (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a0a352e3fe33115133b827b5ad03d99a14101b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964154"
---
# <a name="sdbreadapphelpdetailsdata-function"></a>SdbReadApphelpDetailsData (funzione)

Recupera i dati dal database dettagli apphelp.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Handle per il database di dettagli AppHelp, AppHelp. sdb.

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Struttura [**di \_ dati APPHELP**](apphelp-data.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




