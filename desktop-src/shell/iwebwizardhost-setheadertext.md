---
description: Imposta il titolo e il sottotitolo visualizzati nell'intestazione della procedura guidata. In generale, il client visualizza l'intestazione sopra il codice HTML e sotto la barra del titolo.
title: Metodo WebWizardHost.SetHeaderText (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: d524f9ae6d1031d518e237d393bbb1dc0d35b2bd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841832"
---
# <a name="webwizardhostsetheadertext-method"></a>Metodo WebWizardHost.SetHeaderText

Imposta il titolo e il sottotitolo visualizzati nell'intestazione della procedura guidata. In generale, il client visualizza l'intestazione sopra il codice HTML e sotto la barra del titolo.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrHeaderTitle* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Stringa contenente il titolo.

</dd> <dt>

*bstrHeaderSubtitle* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Stringa contenente il sottotitolo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                            |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 
