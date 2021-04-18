---
title: Proprietà WorkDir di IMsTscSecuredSettings
description: Specifica la directory di lavoro del programma di avvio.
ms.assetid: e67f7274-be47-42c4-9267-a05bb93e6725
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà WorkDir
- Servizi Desktop remoto proprietà WorkDir, interfaccia IMsTscSecuredSettings
- Interfaccia IMsTscSecuredSettings Servizi Desktop remoto, proprietà WorkDir
- Servizi Desktop remoto proprietà WorkDir, interfaccia IMsRdpClientSecuredSettings
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto, proprietà WorkDir
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.WorkDir
- IMsTscSecuredSettings.get_WorkDir
- IMsTscSecuredSettings.put_WorkDir
- IMsRdpClientSecuredSettings.WorkDir
- IMsRdpClientSecuredSettings.get_WorkDir
- IMsRdpClientSecuredSettings.put_WorkDir
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0a80b35ba682012150b4277d800bc4a3582e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302610"
---
# <a name="imstscsecuredsettingsworkdir-property"></a>Proprietà IMsTscSecuredSettings:: WorkDir

Specifica la directory di lavoro del programma di avvio.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_WorkDir(
  [in]  BSTR newVal
);

HRESULT get_WorkDir(
  [out] BSTR *pWorkDir
);
```



## <a name="property-value"></a>Valore proprietà

Nuova directory di lavoro. La lunghezza massima di questa stringa è **Max \_ path**-1 caratteri.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni, vedere [la pagina relativa alla sicurezza dei client RDP](providing-for-rdp-client-security.md) .

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsTscSecuredSettings è definito come c9d65442-A0F9-45b2-8f73-d61d2db8cbb6<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





