---
title: Funzioni TBS
description: TBS fornisce le funzioni seguenti.
ms.assetid: df2d3e36-0a27-4cc0-bcb2-709eb6bedeac
keywords:
- Servizi di base TPM TBS, funzioni
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1b34f2dfbe18ef2230838ff4ba9ec2241d3cc2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399391"
---
# <a name="tbs-functions"></a>Funzioni TBS

TBS fornisce le funzioni seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                       | Descrizione                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Creazione contesto \_ Tbsi**](/windows/desktop/api/Tbs/nf-tbs-tbsi_context_create)<br/>                            | Crea un handle di contesto che può essere usato per passare i comandi a TBS.<br/>                                                                               |
| [**Tbsi \_ creare l' \_ attestazione \_ dal \_ log**](/previous-versions/windows/desktop/legacy/dn455155(v=vs.85))<br/> | Crea un'attestazione estraendo un TrustPoint da un log TCG.<br/>                                                                                |
| [**\_GetDeviceInfo Tbsi**](/windows/desktop/api/Tbs/nf-tbs-tbsi_getdeviceinfo)<br/>                                | Ottiene la versione del TPM nel computer.<br/>                                                                                                  |
| [**Tbsi \_ get \_ OwnerAuth**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_ownerauth)<br/>                               | Recupera l'autorizzazione del proprietario del TPM se le informazioni sono disponibili nel registro di sistema locale. <br/>                                             |
| [**Tbsi \_ ottenere \_ il \_ log TCG**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log)<br/>                                  | Recupera il registro di configurazione di Windows boot più recente (WBCL), noto anche come log TCG.<br/>                                                  |
| [**Tbsi \_ get \_ TCG \_ log \_ es**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log_ex)<br/>                           | Ottiene il log di configurazione di avvio di Windows (WBCL), noto anche come log TCG, del tipo specificato.<br/>                                          |
| [**Tbsi \_ ottenere \_ i \_ log TCG**](/previous-versions/windows/desktop/legacy/dn455156(v=vs.85))<br/>                                | Ottenere uno o più log di configurazione di avvio di Windows (WBCL), detti anche log TCG.<br/>                                                        |
| [**\_ \_ Comando presenza fisica \_ Tbsi**](/windows/desktop/api/Tbs/nf-tbs-tbsi_physical_presence_command)<br/>     | Passa un comando ACPI della presenza fisica attraverso TBS al driver.<br/>                                                                               |
| [**\_ \_ Attestazione revoca Tbsi**](/windows/desktop/api/Tbs/nf-tbs-tbsi_revoke_attestation)<br/>                     | Invalida PCRs se il driver ELAM rileva una violazione dei criteri, ad esempio un rootkit.<br/>                                                     |
| [**\_Comandi di annullamento Tbsip \_**](/windows/desktop/api/Tbs/nf-tbs-tbsip_cancel_commands)<br/>                        | Annulla tutti i comandi in attesa per il contesto specificato.<br/>                                                                                      |
| [**\_Chiusura contesto \_ Tbsip**](/windows/desktop/api/Tbs/nf-tbs-tbsip_context_close)<br/>                            | Chiude un handle del contesto, che rilascia le risorse associate al contesto in TBS e chiude l'handle di associazione utilizzato per comunicare con TBS.<br/> |
| [**\_Comando Invia \_ Tbsip**](/windows/desktop/api/Tbs/nf-tbs-tbsip_submit_command)<br/>                          | Invia un comando di Trusted Platform Module (TPM) a servizi di base TPM (TBS) per l'elaborazione.<br/>                                                       |



 

 

