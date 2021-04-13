---
description: Recupera il numero di provider del servizio di crittografia (CSP).
ms.assetid: 7e0c1613-85ad-4f25-837e-d7b0f11e654a
title: 'Proprietà ISCrdEnr:: CSPCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPCount
- ISCrdEnr.get_CSPCount
- SCrdEnr.CSPCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b2aea22db3c804ae4808996002b68efdcb6cf9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348516"
---
# <a name="iscrdenrcspcount-property"></a>Proprietà ISCrdEnr:: CSPCount

La proprietà **CSPCount** Recupera il numero di [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CSPCount(
   LONG *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Numero di CSP.

## <a name="error-codes"></a>Codici di errore

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr:: NomeCSP**](iscrdenr-cspname.md)
</dt> <dt>

[**ISCrdEnr::enumCSPName**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
