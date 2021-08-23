---
description: Imposta o recupera il nome del provider del servizio di crittografia (CSP).
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: Proprietà ISCrdEnr::CSPName
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
ms.openlocfilehash: 7a1b5b443807dfe7fa737cdfc5eb4da678845e53b555ffe6eebf1529583fdb35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005229"
---
# <a name="iscrdenrcspname-property"></a>Proprietà ISCrdEnr::CSPName

La **proprietà CSPName** imposta o recupera il nome del provider del [*servizio di crittografia*](../secgloss/c-gly.md) (CSP).

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

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni](common-hresult-values.md).

## <a name="remarks"></a>Commenti

Impostare questa proprietà per specificare il nome del provider di servizi di configurazione da usare con il controllo di registrazione smart card. Ottiene questa proprietà per recuperare il nome del provider di servizi di rete specificato. Se non si specifica un valore per questa proprietà, per impostazione predefinita la proprietà **CSPName** viene impostata sul nome nell'elenco disponibile di provider di servizi condivisi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr è definito come \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::CSPCount**](iscrdenr-cspcount.md)
</dt> <dt>

[**ISCrdEnr::enumCSPName**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
