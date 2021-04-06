---
title: Valori del registro di sistema del protocollo di autenticazione
description: Il software di installazione per la DLL EAP può creare i seguenti valori del registro di sistema eaptypeid.
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8091197c7b0d5c5a208bf3658bbc15284a29ac9e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104046154"
---
# <a name="authentication-protocol-registry-values"></a>Valori del registro di sistema del protocollo di autenticazione

Il software di installazione per la DLL EAP può creare i seguenti valori del registro di sistema **&lt; eaptypeid &gt;**. Questi valori del registro di sistema sono definiti nel file di intestazione Raseapif. h. I valori **RAS_EAP_VALUENAME_PATH** e **RAS_EAP_VALUENAME_FRIENDLY_NAME** sono obbligatori. Il software di installazione può anche creare altre chiavi e valori. Questi possono essere usati dal protocollo di autenticazione stesso. Per ulteriori informazioni e un esempio di configurazione del registro di sistema, vedere [esempio di valori del registro di sistema](registry-values-example.md).

[RAS_EAP_VALUENAME_PATH](#ras_eap_valuename_path)

[RAS_EAP_VALUENAME_FRIENDLY_NAME](#ras_eap_valuename_friendly_name)

[RAS_EAP_VALUENAME_CONFIGUI](#ras_eap_valuename_configui)

[RAS_EAP_VALUENAME_DEFAULT_DATA](#ras_eap_valuename_default_data)

[RAS_EAP_VALUENAME_REQUIRE_CONFIGUI](#ras_eap_valuename_require_configui)

[RAS_EAP_VALUENAME_CONFIG_CLSID](#ras_eap_valuename_config_clsid)

[RAS_EAP_VALUENAME_IDENTITY](#ras_eap_valuename_identity)

[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) I

[RAS_EAP_VALUENAME_INVOKE_NAMEDLG](#ras_eap_valuename_invoke_namedlg)

[RAS_EAP_VALUENAME_INVOKE_PWDDLG](#ras_eap_valuename_invoke_pwddlg)

[RAS_EAP_VALUENAME_ENCRYPTION](#ras_eap_valuename_encryption)

[RAS_EAP_VALUENAME_STANDALONE_SUPPORTED](#ras_eap_valuename_standalone_supported)

[RAS_EAP_VALUENAME_ROLES_SUPPORTED](#ras_eap_valuename_roles_supported)

[RAS_EAP_VALUENAME_PER_POLICY_CONFIG](#ras_eap_valuename_per_policy_config)

[RAS_EAP_VALUENAME_ISTUNNEL_METHOD](#ras_eap_valuename_istunnel_method)

[RAS_EAP_VALUENAME_FILTER_INNERMETHODS](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a>RAS_EAP_VALUENAME_PATH

| Valore costante | Percorso                               |
|----------------|------------------------------------|
| Tipo           | REG_EXPAND_SZ                    |
| Descrizione    | Specifica il percorso della DLL EAP. |

## <a name="ras_eap_valuename_friendly_name"></a>RAS_EAP_VALUENAME_FRIENDLY_NAME

| Valore costante | FriendlyName                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_SZ                                                                                                                                                           |
| Descrizione    | Specifica un nome descrittivo per il protocollo di autenticazione. Questo nome viene visualizzato nell'interfaccia utente dell'applicazione EAP per le implementazioni remote e wireless. |

## <a name="ras_eap_valuename_configui"></a>RAS_EAP_VALUENAME_CONFIGUI

| Valore costante | ConfigUIPath                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_EXPAND_SZ                                                                                                                   |
| Descrizione    | Specifica il percorso della DLL che implementa l'interfaccia utente di configurazione nel client, perché questa interfaccia utente è solo per il client. |

## <a name="ras_eap_valuename_default_data"></a>RAS_EAP_VALUENAME_DEFAULT_DATA

| Valore costante | ConfigData                                                            |
|----------------|-----------------------------------------------------------------------|
| Tipo           | REG_BINARY                                                           |
| Descrizione    | Specifica i dati di configurazione predefiniti per il protocollo di autenticazione. |

## <a name="ras_eap_valuename_require_configui"></a>RAS_EAP_VALUENAME_REQUIRE_CONFIGUI

| Valore costante | RequireConfigUI                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                                                                               |
| Descrizione    | Specifica se l'utente deve fornire i dati di configurazione nell'interfaccia utente dell'applicazione client EAP. Se questo valore è 1, l'utente non è autorizzato a uscire dall'interfaccia utente dell'applicazione client EAP senza fornire i dati di configurazione. Il valore predefinito è 0. |

## <a name="ras_eap_valuename_config_clsid"></a>RAS_EAP_VALUENAME_CONFIG_CLSID

| Valore costante | ConfigCLSID                                                   |
|----------------|---------------------------------------------------------------|
| Tipo           | REG_SZ                                                       |
| Descrizione    | Specifica l'ID classe dell'interfaccia utente di configurazione nel server. |

## <a name="ras_eap_valuename_identity"></a>RAS_EAP_VALUENAME_IDENTITY

| Valore costante | IdentityPath                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_EXPAND_SZ                                                                                                                        |
| Descrizione    | Specifica il percorso della DLL che implementa le funzioni per ottenere l'identità utente nel client, perché questa interfaccia utente è destinata solo ai client. |

## <a name="ras_eap_valuename_interactiveui"></a>RAS_EAP_VALUENAME_INTERACTIVEUI

| Valore costante | InteractiveUIPath                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_EXPAND_SZ                                                                                                                 |
| Descrizione    | Specifica il percorso della DLL che implementa l'interfaccia utente interattiva sul client perché questa interfaccia utente è solo per il client. |

## <a name="ras_eap_valuename_invoke_namedlg"></a>RAS_EAP_VALUENAME_INVOKE_NAMEDLG

| Valore costante | InvokeUsernameDialog                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                             |
| Descrizione    | Specifica se RAS deve visualizzare la finestra di dialogo del nome utente standard di Windows NT/Windows 2000 (valore 1) o richiamare [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (valore 0). Il valore predefinito è 1. |

## <a name="ras_eap_valuename_invoke_pwddlg"></a>RAS_EAP_VALUENAME_INVOKE_PWDDLG

| Valore costante | InvokePasswordDialog                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                  |
| Descrizione    | Specifica se RAS deve visualizzare la finestra di dialogo della password standard di Windows NT/Windows 2000. Se questo valore esiste e è 0, RAS non visualizzerà la finestra di dialogo password. Il valore predefinito è 1. |


## <a name="ras_eap_valuename_encryption"></a>RAS_EAP_VALUENAME_ENCRYPTION

| Valore costante | MPPEEncryptionSupported                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                    |
| Descrizione    | Se questo valore è 1, il protocollo di autenticazione può generare chiavi per lo stile di crittografia Point-to-Point Encryption (MPPE) di Microsoft. I valori possibili sono 0 o 1. Il valore predefinito è 0. |

## <a name="ras_eap_valuename_standalone_supported"></a>RAS_EAP_VALUENAME_STANDALONE_SUPPORTED

| Valore costante | StandaloneSupported                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                     |
| Descrizione    | Specifica se il protocollo di autenticazione è supportato in un server Windows 2000 autonomo. Il valore 0 indica che il protocollo EAP non è supportato. Il valore predefinito è 1. |

## <a name="ras_eap_valuename_roles_supported"></a>RAS_EAP_VALUENAME_ROLES_SUPPORTED

| Constant Value | RolesSupported                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                                                                 |
| Descrizione    | Specifica i vari ruoli supportati da EAP. Indica se può essere utilizzato in un server o in un client, se è supportato per le connessioni RAS (VPN) o PEAP. Il comportamento predefinito prevede la visualizzazione del metodo EAP in PEAP e in EAP. |

## <a name="ras_eap_valuename_per_policy_config"></a>RAS_EAP_VALUENAME_PER_POLICY_CONFIG

| Constant Value | PerPolicyConfig |
|----------------|-----------------|
| Tipo           | REG_DWORD      |
| Descrizione    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a>RAS_EAP_VALUENAME_ISTUNNEL_METHOD

Il valore del registro di sistema non è in uso.

## <a name="ras_eap_valuename_filter_innermethods"></a>RAS_EAP_VALUENAME_FILTER_INNERMETHODS

Il valore del registro di sistema non è in uso.

