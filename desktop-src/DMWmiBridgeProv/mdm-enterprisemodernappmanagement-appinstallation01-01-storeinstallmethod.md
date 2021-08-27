---
title: Metodo StoreInstallMethod della classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Metodo per eseguire un'installazione di un'app e una licenza dal Windows Store. Vedere anche StoreInstall.
ms.assetid: 4f8aff47-ad16-4fe5-85be-7ddb55ddff24
keywords:
- Metodo StoreInstallMethod
- Metodo StoreInstallMethod, MDM_EnterpriseModernAppManagement_AppInstallation01_01 classe
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 classe, metodo StoreInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.StoreInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a8e60134da45982773c0219ade8e0e0f12f37ec9e6d16cd97f4595ae8b507a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084941"
---
# <a name="storeinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>Metodo StoreInstallMethod della classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Metodo per eseguire un'installazione di un'app e una licenza dal Windows Store. Vedere anche [StoreInstall.](/windows/client-management/mdm/enterprisemodernappmanagement-csp)

## <a name="syntax"></a>Sintassi


```mof
uint32 StoreInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*param* \[ Pollici\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

