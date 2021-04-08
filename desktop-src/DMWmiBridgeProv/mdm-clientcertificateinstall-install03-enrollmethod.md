---
title: Metodo EnrollMethod della classe MDM_ClientCertificateInstall_Install03
description: Attiva il dispositivo per avviare la registrazione del certificato.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Metodo EnrollMethod
- Metodo EnrollMethod, classe MDM_ClientCertificateInstall_Install03
- Classe MDM_ClientCertificateInstall_Install03, metodo EnrollMethod
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
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742639"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a>Metodo EnrollMethod della classe MDM \_ ClientCertificateInstall \_ Install03

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Attiva il dispositivo per avviare la registrazione del certificato. Al termine della registrazione del certificato, il dispositivo non invierà una notifica al server MDM. Il server MDM potrebbe successivamente eseguire una query sul dispositivo per verificare se è stato aggiunto un nuovo certificato. Vedere anche [**registrazione**](/windows/client-management/mdm/clientcertificateinstall-csp).

## <a name="syntax"></a>Sintassi


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Obbligatorio. Attiva il dispositivo per avviare la registrazione del certificato. Al termine della registrazione del certificato, il dispositivo non invierà una notifica al server MDM. Il server MDM potrebbe successivamente eseguire una query sul dispositivo per verificare se è stato aggiunto un nuovo certificato.

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

[**\_Install03 CLIENTCERTIFICATEINSTALL \_ MDM**](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[Utilizzo di script di PowerShell con il provider del Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

