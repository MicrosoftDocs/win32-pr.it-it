---
title: Classe MDM_ClientCertificateInstall_Install03
description: La \_ classe MDM ClientCertificateInstall \_ Install03 consente all'organizzazione di impostare l'installazione dei certificati client.
ms.assetid: 0083e54c-e621-47da-a20d-17c8bbf7dd3a
keywords:
- Classe MDM_ClientCertificateInstall_Install03
- Classe MDM_ClientCertificateInstall_Install03, descritta
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03
- MDM_ClientCertificateInstall_Install03.InstanceID
- MDM_ClientCertificateInstall_Install03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ac690808551e05d6ceba4f3c84bcaa521d4d01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120663"
---
# <a name="mdm_clientcertificateinstall_install03-class"></a>\_Classe MDM ClientCertificateInstall \_ Install03

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe **MDM \_ ClientCertificateInstall \_ Install03** consente all'organizzazione di impostare l'installazione dei certificati client. Obbligatorio per la registrazione del certificato SCEP. Nodo padre per raggruppare la richiesta relativa all'installazione del certificato SCEP.

> [!Note]  
> Anche se i nodi figlio in installazione supportano i comandi Replace, dopo l'invio del comando exec al dispositivo, il dispositivo utilizzerà i valori impostati quando il comando exec viene accettato. Il server non deve aspettarsi che la modifica del valore del nodo dopo l'accettazione del comando exec influirà sulla registrazione in corso. Il server deve verificare il valore del nodo stato e assicurarsi che il dispositivo non sia in fase sconosciuta prima di modificare i valori del nodo figlio.

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_Install03
{
  string InstanceID;
  string ParentID;
  string ServerURL;
  string Challenge;
  string EKUMapping;
  sint32 KeyUsage;
  string SubjectName;
  sint32 KeyProtection;
  sint32 RetryDelay;
  sint32 RetryCount;
  string TemplateName;
  sint32 KeyLength;
  string HashAlgorithm;
  string CAThumbprint;
  string SubjectAlternativeNames;
  string ValidPeriod;
  sint32 ValidPeriodUnits;
  string ContainerName;
  string CustomTextToShowInPrompt;
  string AADKeyIdentifierList;
};
```

## <a name="members"></a>Members

La classe **MDM \_ ClientCertificateInstall \_ Install03** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **MDM \_ ClientCertificateInstall \_ Install03** ha questi metodi.



| Metodo                                                                      | Descrizione                                                                   |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**EnrollMethod**](mdm-clientcertificateinstall-install03-enrollmethod.md) | Obbligatorio. Attiva il dispositivo per avviare la registrazione del certificato.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **MDM \_ ClientCertificateInstall \_ Install03** dispone di queste proprietà.

<dl> <dt>

[AADKeyIdentifierList](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-aadkeyidentifierlist)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[Identificazione personale](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-cathumbprint)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[Sfida](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-challenge)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ContainerName](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[CustomTextToShowInPrompt](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-customtexttoshowinprompt)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[EKUMapping](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-ekumapping)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[HashAlgorithm](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-hashalgorithm)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obbligatorio per la registrazione del certificato SCEP. Nodo padre per raggruppare la richiesta relativa all'installazione del certificato SCEP.

Il formato è node.

</dd> <dt>

[KeyLength](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keylength)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[Protezione di dati](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keyprotection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[KeyUsage](/windows/client-management/mdm/clientcertificateinstall-csp)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre.

La stringa è "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueId*"

</dd> <dt>

[RetryCount](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrycount)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[RetryDelay](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrydelay)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ServerURL](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-serverurl)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[SubjectAlternativeNames](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectalternativenames)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[SubjectName](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectname)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[TemplateName](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-templatename)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ValidPeriod](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiod)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ValidPeriodUnits](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiodunits)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> </dl>

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

[Utilizzo di script di PowerShell con il provider del Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

