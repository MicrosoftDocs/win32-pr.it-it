---
description: Specifica il nome dell'autorità di certificazione (CA).
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'Metodo ISCrdEnr:: setCAName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316659"
---
# <a name="iscrdenrsetcaname-method"></a>Metodo ISCrdEnr:: setCAName

Il metodo **setCAName** specifica il nome dell' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).

## <a name="syntax"></a>Sintassi


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Valore che specifica se il nome fa riferimento al nome della CA o al nome del computer della CA. Se questo valore viene spaventato \_ , registrare il \_ nome del computer della CA \_ \_ (definito come 0x01), il nome si riferisce al nome del computer della CA. In caso contrario, il nome fa riferimento al nome della CA.

</dd> <dt>

*bstrCertTemplateName* \[ in\]
</dt> <dd>

Nome del modello di certificato.

</dd> <dt>

*bstrCAName* \[ in\]
</dt> <dd>

Nome della CA da usare con il modello di certificato specificato da *bstrCertTemplateName*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="vb"></a>VB

Il valore restituito è un valore **HRESULT**. Un valore di S \_ OK indica che la chiamata ha avuto esito positivo.

## <a name="remarks"></a>Commenti

Utilizzare questo metodo per specificare una CA per un modello di certificato.

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

[**ISCrdEnr::enumCAName**](iscrdenr-enumcaname.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
