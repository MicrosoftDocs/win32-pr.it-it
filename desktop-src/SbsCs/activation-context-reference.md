---
description: Le funzioni e le strutture del contesto di attivazione vengono utilizzate con gli assembly affiancati.
ms.assetid: b53b30e0-948e-406c-9fb4-9681dc3c5670
title: Riferimento al contesto di attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f8225b4db8b22227edf2b779ed9e1b50da7a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049981"
---
# <a name="activation-context-reference"></a>Riferimento al contesto di attivazione

Le funzioni e le strutture del contesto di attivazione vengono utilizzate con gli assembly affiancati.

Nella tabella seguente sono elencate le funzioni del contesto di attivazione.



| Funzione                                                   | Descrizione                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx)                   | Attiva il contesto di attivazione specificato.                                                                                                             |
| [**AddRefActCtx**](/windows/desktop/api/Winbase/nf-winbase-addrefactctx)                       | Incrementa il conteggio dei riferimenti del contesto di attivazione specificato.                                                                                     |
| [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)                       | Crea un contesto di attivazione.                                                                                                                          |
| [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx)               | Disattiva il contesto di attivazione specificato.                                                                                                           |
| [**FindActCtxSectionGuid**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionguid)     | Restituisce i dati contenuti nella [**sezione ACTCTX struttura di \_ \_ \_ dati con chiave**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) corrispondente al GUID specificato.   |
| [**FindActCtxSectionString**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionstringa) | Restituisce i dati contenuti nella [**sezione ACTCTX struttura di \_ \_ \_ dati con chiave**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) corrispondente alla stringa specificata. |
| [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx)               | Restituisce il contesto di attivazione corrente.                                                                                                                 |
| [**IsolationAwareCleanup**](/previous-versions/windows/desktop/legacy/aa375204(v=vs.85))     | Garantisce che la memoria venga liberata quando un manifesto viene caricato, scaricato e ricaricato.                                                                         |
| [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)                       | Esegue una query sul contesto di attivazione per ottenere informazioni su un assembly o un file.                                                                               |
| [**QueryActCtxSettingsW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxsettingsw)       | Specifica lo spazio dei nomi e il nome dell'attributo su cui eseguire una query.                                                                      |
| [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)                     | Decrementa il conteggio dei riferimenti del contesto di attivazione specificato.                                                                                     |
| [**ZombifyActCtx**](/windows/desktop/api/Winbase/nf-winbase-zombifyactctx)                     | Disattiva il contesto di attivazione specificato, ma non lo dealloca.                                                                               |



 

Nella tabella seguente sono elencate le strutture del contesto di attivazione.



| Struttura                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ informazioni dettagliate sull'assembly del contesto \_ di attivazione**](/windows/desktop/api/Winnt/ns-winnt-activation_context_assembly_detailed_information) | Contiene informazioni dettagliate sul contesto di attivazione.                                                                                                                                                                                                                                                                                                                                  |
| [**\_ \_ informazioni dettagliate sul contesto di \_ attivazione**](/windows/desktop/api/Winnt/ns-winnt-activation_context_detailed_information)                    | Contiene informazioni sull'assembly nel contesto di attivazione.                                                                                                                                                                                                                                                                                                                           |
| [**\_ \_ Indice query contesto di attivazione \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_query_index)                                      | Contiene l'assembly all'interno del contesto di attivazione e l'indice del file all'interno dell'assembly.                                                                                                                                                                                                                                                                                           |
| [**ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctxa)                                                                                     | Contiene informazioni che descrivono un contesto di attivazione specifico.                                                                                                                                                                                                                                                                                                                           |
| [**\_dati con \_ chiave della sezione ACTCTX \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data)                                            | Restituisce le informazioni sul contesto di attivazione insieme alla sezione del contesto di attivazione con tag Integer a 32 bit.                                                                                                                                                                                                                                                                   |
| [**\_ \_ informazioni dettagliate sul file di \_ assembly**](/windows/desktop/api/Winnt/ns-winnt-assembly_file_detailed_information)                              | Contiene informazioni su un file dell'assembly nel contesto di attivazione.                                                                                                                                                                                                                                                                                                                 |
| [**\_ \_ \_ informazioni sul livello di esecuzione del contesto di attivazione \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_run_level_information)                 | Usato dalla funzione [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) .<br/> **Windows Server 2003 e Windows XP:** Questa struttura non è disponibile.<br/>                                                                                                                                                                                                                                    |
| [**\_elemento del contesto di compatibilità \_**](/windows/desktop/api/Winnt/ns-winnt-compatibility_context_element)                                         | Utilizzato dalla funzione [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) come parte della struttura delle [**\_ informazioni di \_ compatibilità \_ del contesto di attivazione**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information) . <br/> **Windows Server 2008 e versioni precedenti e Windows Vista e versioni precedenti:** Questa struttura non è disponibile. È disponibile a partire da Windows Server 2008 R2 e Windows 7.<br/> |
| [**\_ \_ informazioni sulla compatibilità del contesto di attivazione \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information)          | Usato dalla funzione [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) .<br/> **Windows Server 2008 e versioni precedenti e Windows Vista e versioni precedenti:** Questa struttura non è disponibile. È disponibile a partire da Windows Server 2008 R2 e Windows 7.<br/>                                                                                                                                   |



 

Nella tabella seguente sono elencate le enumerazioni del contesto di attivazione.

| Enumerazione                                                                       | Descrizione                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACTCTX \_ a \_ livello di esecuzione richiesto \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_requested_run_level)               | Descrive il livello di esecuzione richiesto del contesto di attivazione. **Windows Server 2003 e Windows XP:** Questa enumerazione non è disponibile.<br/>                                                                                                      |
| [**\_tipo di \_ elemento di compatibilità ACTCTX \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_compatibility_element_type) | Descrive l'elemento Compatibility nel manifesto dell'applicazione. **Windows Server 2008 e versioni precedenti e Windows Vista e versioni precedenti:** Questa enumerazione non è disponibile. È disponibile a partire da Windows Server 2008 R2 e Windows 7.<br/> |



 

 

