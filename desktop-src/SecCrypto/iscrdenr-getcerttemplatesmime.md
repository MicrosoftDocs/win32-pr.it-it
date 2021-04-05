---
description: Usato per determinare se un modello di certificato contiene l' \_ \_ utilizzo della \_ chiave di protezione della posta elettronica szOID PKIX KP \_ .
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'Metodo ISCrdEnr:: getCertTemplateSMIME'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884042"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a>Metodo ISCrdEnr:: getCertTemplateSMIME

Il metodo **getCertTemplateSMIME** viene usato per determinare se un modello di certificato contiene l' \_ utilizzo della chiave di protezione della posta elettronica di szOID PKIX \_ KP \_ \_ .

Se questo utilizzo della chiave fa parte del modello di certificato, il modello di certificato supporta le operazioni [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME).

## <a name="syntax"></a>Sintassi


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrCertTemplateName* \[ in\]
</dt> <dd>

Nome del certificato sottoposto a query per l'utilizzo della chiave S/MIME.

</dd> <dt>

*pdwCertTemplateSMIME* \[ out\]
</dt> <dd>

Puntatore a un valore **DWORD** che restituisce un valore di uno se *bstrCertTemplateName* supporta S/MIME. in caso contrario, restituisce zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Valore **Long** di uno se *bstrCertTemplateName* supporta S/MIME; in caso contrario, zero.

## <a name="remarks"></a>Commenti

La costante per szOID \_ PKIX \_ KP \_ email \_ Protection è definita in WinCrypt. h.

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

[**ISCrdEnr:: registra**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
