---
description: Usato per determinare se un modello di certificato contiene l'utilizzo della chiave SzOID \_ PKIX \_ KP \_ EMAIL \_ PROTECTION.
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: Metodo ISCrdEnr::getCertTemplateSMIME
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
ms.openlocfilehash: 8da8c9c3202c0955a001a63e77f85858fc6237d7476c0fc5222ae8f85e94a7c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515961"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a>Metodo ISCrdEnr::getCertTemplateSMIME

Il **metodo getCertTemplateSMIME** viene usato per determinare se un modello di certificato contiene l'utilizzo della chiave DI POSTA ELETTRONICA \_ PKIX SZOID. \_ \_ \_

Se l'utilizzo della chiave fa parte del modello di certificato, il modello di certificato supporta le operazioni [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME).

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

*bstrCertTemplateName* \[ Pollici\]
</dt> <dd>

Nome del certificato sottoposto a query per l'utilizzo della chiave S/MIME.

</dd> <dt>

*pdwCertTemplateSMIME* \[ Cambio\]
</dt> <dd>

Puntatore a **un valore DWORD** che restituisce un valore pari a uno se *bstrCertTemplateName* supporta S/MIME; In caso contrario, restituisce zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](common-hresult-values.md)

### <a name="vb"></a>VB

**Valore** long di uno se *bstrCertTemplateName* supporta S/MIME; in caso contrario zero.

## <a name="remarks"></a>Commenti

La costante per szOID \_ PKIX \_ KP \_ EMAIL PROTECTION è definita \_ in Wincrypt.h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr è definito come 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
