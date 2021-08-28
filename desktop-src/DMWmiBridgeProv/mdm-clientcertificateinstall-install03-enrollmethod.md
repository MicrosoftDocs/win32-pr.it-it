---
title: Metodo EnrollMethod della MDM_ClientCertificateInstall_Install03 classe
description: Attiva il dispositivo per avviare la registrazione del certificato.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Metodo EnrollMethod
- Metodo EnrollMethod, MDM_ClientCertificateInstall_Install03 classe
- MDM_ClientCertificateInstall_Install03 classe, metodo EnrollMethod
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeca621f58015aa3806212c1250aeb43554a51cbb28e15414e779571b9c102
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109401"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a>Metodo EnrollMethod della classe \_ MDM ClientCertificateInstall \_ Install03

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Attiva il dispositivo per avviare la registrazione del certificato. Il dispositivo non invierà notifiche al server MDM al termine della registrazione del certificato. Il server MDM potrebbe successivamente eseguire una query sul dispositivo per determinare se viene aggiunto un nuovo certificato. Vedere anche [**Registrare**](/windows/client-management/mdm/clientcertificateinstall-csp).

## <a name="syntax"></a>Sintassi


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Obbligatorio. Attiva il dispositivo per avviare la registrazione del certificato. Il dispositivo non invierà notifiche al server MDM al termine della registrazione del certificato. Il server MDM potrebbe successivamente eseguire una query sul dispositivo per determinare se viene aggiunto un nuovo certificato.

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

[**Client \_ \_ MDMInstallare l'installazione03**](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

