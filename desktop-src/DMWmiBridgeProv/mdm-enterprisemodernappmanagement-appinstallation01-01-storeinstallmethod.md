---
title: Metodo StoreInstallMethod della classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Metodo per eseguire un'installazione di un'app e una licenza da Windows Store. Vedere anche StoreInstall.
ms.assetid: 4f8aff47-ad16-4fe5-85be-7ddb55ddff24
keywords:
- Metodo StoreInstallMethod
- Metodo StoreInstallMethod, classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, metodo StoreInstallMethod
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
ms.openlocfilehash: 4c4ae34e8502b7d408a7fb4d96fb9c2c4fadb509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964617"
---
# <a name="storeinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>Metodo StoreInstallMethod della classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Metodo per eseguire un'installazione di un'app e una licenza da Windows Store. Vedere anche [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).

## <a name="syntax"></a>Sintassi


```mof
uint32 StoreInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*param* \[ in\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[Utilizzo di script di PowerShell con il provider del Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

