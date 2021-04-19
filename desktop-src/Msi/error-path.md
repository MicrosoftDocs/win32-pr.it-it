---
description: In Windows Installer versioni 1,0 e 1,1 la proprietà Path è sempre la stringa vuota. Le versioni future possono usare questo valore per restituire il percorso del file o della directory che non è stato possibile creare.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Proprietà Error. Path (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5a2e462790d6f929943fe2fe364228cd73d3deb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326377"
---
# <a name="errorpath-property"></a>Proprietà Error. Path

In Windows Installer versioni 1,0 e 1,1 la proprietà Path è sempre la stringa vuota. Le versioni future possono usare questo valore per restituire il percorso del file o della directory che non è stato possibile creare.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Error.Path
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Questo valore è valido solo per errori di tipo msmErrorFileCreate o msmErrorDirCreate. È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .

### <a name="c"></a>C++

Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) la funzione PATH.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

