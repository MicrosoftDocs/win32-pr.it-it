---
description: Imposta o Recupera il nome del provider del servizio di crittografia (CSP).
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: 'Proprietà ISCrdEnr:: NomeCSP'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 363f2f9120d3b0a202335d0e8e450464cbc1f118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058182"
---
# <a name="iscrdenrcspname-property"></a>Proprietà ISCrdEnr:: NomeCSP

La proprietà **NomeCSP** imposta o Recupera il nome del [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Nome del CSP.

## <a name="error-codes"></a>Codici di errore

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

## <a name="remarks"></a>Commenti

Impostare questa proprietà per specificare il nome del CSP da usare con il controllo di registrazione delle smart card. Ottenere questa proprietà per recuperare il nome del CSP specificato. Se non si specifica un valore per questa proprietà, per impostazione predefinita la proprietà **NomeCSP** viene impostata sul nome nell'elenco dei CSP disponibili.

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

[**ISCrdEnr::CSPCount**](iscrdenr-cspcount.md)
</dt> <dt>

[**ISCrdEnr::enumCSPName**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
