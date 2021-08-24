---
title: Metodo HostedInstallMethod della classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Metodo per eseguire un'installazione di un pacchetto dell'app da un percorso ospitato, ad esempio un'unità locale, un'origine dati UNC o HTTPS. Vedere anche HostedInstall.
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- Metodo HostedInstallMethod
- Metodo HostedInstallMethod, MDM_EnterpriseModernAppManagement_AppInstallation01_01 classe
- MDM_EnterpriseModernAppManagement_AppInstallation01_01, metodo HostedInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60cd27419dce09b2a0e4aa7304bb53ac63e7d205b93cbaacbf832aa4a3501338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750631"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>Metodo HostedInstallMethod della classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Metodo per eseguire un'installazione di un pacchetto dell'app da un percorso ospitato, ad esempio un'unità locale, un'origine dati UNC o HTTPS. Vedere anche [HostedInstall.](/windows/client-management/mdm/enterprisemodernappmanagement-csp)

## <a name="syntax"></a>Sintassi


```mof
uint32 HostedInstallMethod(
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

 

