---
description: Imposta o recupera un valore booleano che specifica se è possibile utilizzare i prompt dell'interfaccia utente per l'identità di un firmatario o di un mittente.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Proprietà Settings. EnablePromptForCertificateUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329464"
---
# <a name="settingsenablepromptforcertificateui-property"></a>Proprietà Settings. EnablePromptForCertificateUI

\[La proprietà **EnablePromptForCertificateUI** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]

La proprietà **EnablePromptForCertificateUI** imposta o recupera un valore booleano che specifica se è possibile utilizzare i prompt dell'interfaccia utente per l'identità di un firmatario o di un mittente.

## <a name="syntax"></a>Sintassi


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se è **true**, è possibile usare l'identità dell'interfaccia utente per un firmatario o un mittente. Il valore predefinito è **false**.

> [!Note]  
> L'impostazione di questa proprietà non disabilita gli avvisi generati prima che l'utilizzo della chiave privata venga eseguito da un'applicazione basata sul Web.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni**](settings.md)
</dt> </dl>

 

 




