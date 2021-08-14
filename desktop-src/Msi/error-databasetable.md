---
description: La proprietà DatabaseTable di sola lettura dell'oggetto Error restituisce il nome della tabella nel database che ha causato l'errore.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Proprietà Error.DatabaseTable (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: b9e52523b37c90de4c4592fdeb059e6269f4e05e240242e69e14f0be6d4d53a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378172"
---
# <a name="errordatabasetable-property"></a>Error.DatabaseTable - proprietà

La proprietà **DatabaseTable di** sola lettura [**dell'oggetto Error**](error-object.md) restituisce il nome della tabella nel database che ha causato l'errore.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

La raccolta è vuota se i valori non si applicano al tipo di errore. È possibile determinare il tipo di errore chiamando [**la proprietà Type**](error-type.md) dell'oggetto [**Error.**](error-object.md)

### <a name="c"></a>C++

Vedere [**la funzione get \_ DatabaseTable.**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

