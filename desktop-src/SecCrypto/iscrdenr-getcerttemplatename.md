---
description: Recupera il nome del modello di certificato.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'Metodo ISCrdEnr:: getCertTemplateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233499"
---
# <a name="iscrdenrgetcerttemplatename-method"></a>Metodo ISCrdEnr:: getCertTemplateName

Il metodo **getCertTemplateName** Recupera il nome del modello di certificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Valore che determina se viene restituito il nome reale o il nome visualizzato del modello di certificato. Se *dwFlags* presenta il valore SCard \_ Registra \_ il \_ \_ nome visualizzato del modello \_ di certificato, viene recuperato il nome visualizzato del modello di certificato; in caso contrario, viene visualizzato il nome effettivo del modello di certificato.

</dd> <dt>

*pbstrCertTemplateName* \[ out\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome del modello di certificato che verrà usato nella [*richiesta di certificato*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Stringa che rappresenta il nome del modello di certificato che verrà utilizzato nella [*richiesta di certificato*](../secgloss/c-gly.md).

## <a name="remarks"></a>Commenti

Se non si imposta il nome del modello di certificato chiamando [**ISCrdEnr:: setCertTemplateName**](iscrdenr-setcerttemplatename.md), il nome predefinito è il primo nome nell'elenco dei modelli di certificato disponibili.

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

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
