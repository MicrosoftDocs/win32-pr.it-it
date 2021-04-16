---
description: Enumera il nome dei provider del servizio di crittografia (CSP) disponibili.
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: 'Metodo ISCrdEnr:: enumCSPName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529994"
---
# <a name="iscrdenrenumcspname-method"></a>Metodo ISCrdEnr:: enumCSPName

Il metodo **enumCSPName** enumera il nome dei [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) disponibili.

## <a name="syntax"></a>Sintassi


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Indice in base zero per la sequenza di enumerazione.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Riservato per utilizzi futuri. Impostare questo valore su zero.

</dd> <dt>

*pbstrCSPName* \[ out\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome del CSP enumerato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Stringa che rappresenta il nome del CSP enumerato.

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

[**ISCrdEnr:: NomeCSP**](iscrdenr-cspname.md)
</dt> </dl>

 

 
