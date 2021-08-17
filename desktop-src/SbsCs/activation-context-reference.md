---
description: Le funzioni e le strutture del contesto di attivazione vengono usate con assembly side-by-side.
ms.assetid: b53b30e0-948e-406c-9fb4-9681dc3c5670
title: Informazioni di riferimento sul contesto di attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72eb4bc136a95766a62bb96e67ac198f88fca905c60ba98e6bf922ce65a36389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142584"
---
# <a name="activation-context-reference"></a>Informazioni di riferimento sul contesto di attivazione

Le funzioni e le strutture del contesto di attivazione vengono usate con assembly side-by-side.

Nella tabella seguente sono elencate le funzioni del contesto di attivazione.



| Funzione                                                   | Descrizione                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx)                   | Attiva il contesto di attivazione specificato.                                                                                                             |
| [**AddRefActCtx**](/windows/desktop/api/Winbase/nf-winbase-addrefactctx)                       | Incrementa il conteggio dei riferimenti del contesto di attivazione specificato.                                                                                     |
| [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)                       | Crea un contesto di attivazione.                                                                                                                          |
| [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx)               | Disattiva il contesto di attivazione specificato.                                                                                                           |
| [**FindActCtxSectionGuid**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionguid)     | Restituisce i dati contenuti nella [**struttura \_ ACTCTX SECTION \_ KEYED \_ DATA**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) che corrisponde al GUID specificato.   |
| [**FindActCtxSectionString**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionstringa) | Restituisce i dati contenuti nella [**struttura \_ ACTCTX SECTION \_ KEYED \_ DATA**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) che corrisponde alla stringa specificata. |
| [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx)               | Restituisce il contesto di attivazione corrente.                                                                                                                 |
| [**IsolationAwareCleanup**](/previous-versions/windows/desktop/legacy/aa375204(v=vs.85))     | Assicura che la memoria sia liberata quando un manifesto viene caricato, scaricato e ricaricato.                                                                         |
| [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)                       | Esegue una query sul contesto di attivazione per ottenere informazioni su un assembly o un file.                                                                               |
| [**QueryActCtxSettingsW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxsettingsw)       | Specifica lo spazio dei nomi e il nome dell'attributo su cui eseguire la query.                                                                      |
| [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)                     | Decrementa il conteggio dei riferimenti del contesto di attivazione specificato.                                                                                     |
| [**ZombifyActCtx**](/windows/desktop/api/Winbase/nf-winbase-zombifyactctx)                     | Disattiva il contesto di attivazione specificato, ma non lo dealloca.                                                                               |



 

Nella tabella seguente sono elencate le strutture del contesto di attivazione.



| Struttura                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INFORMAZIONI \_ \_ DETTAGLIATE SULL'ASSEMBLY \_ DEL CONTESTO DI \_ ATTIVAZIONE**](/windows/desktop/api/Winnt/ns-winnt-activation_context_assembly_detailed_information) | Contiene informazioni dettagliate sul contesto di attivazione.                                                                                                                                                                                                                                                                                                                                  |
| [**INFORMAZIONI \_ DETTAGLIATE \_ SUL CONTESTO DI \_ ATTIVAZIONE**](/windows/desktop/api/Winnt/ns-winnt-activation_context_detailed_information)                    | Contiene informazioni sull'assembly nel contesto di attivazione.                                                                                                                                                                                                                                                                                                                           |
| [**INDICE DELLA \_ QUERY DEL CONTESTO DI \_ \_ ATTIVAZIONE**](/windows/desktop/api/Winnt/ns-winnt-activation_context_query_index)                                      | Contiene l'assembly all'interno del contesto di attivazione e l'indice del file all'interno dell'assembly.                                                                                                                                                                                                                                                                                           |
| [**ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctxa)                                                                                     | Contiene informazioni che descrivono un contesto di attivazione specifico.                                                                                                                                                                                                                                                                                                                           |
| [**DATI CON CHIAVE DELLA SEZIONE ACTCTX \_ \_ \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data)                                            | Restituisce le informazioni sul contesto di attivazione insieme al GUID o alla sezione del contesto di attivazione con tag integer a 32 bit.                                                                                                                                                                                                                                                                   |
| [**INFORMAZIONI \_ DETTAGLIATE SUL FILE \_ DI \_ ASSEMBLY**](/windows/desktop/api/Winnt/ns-winnt-assembly_file_detailed_information)                              | Contiene informazioni su un file dell'assembly nel contesto di attivazione.                                                                                                                                                                                                                                                                                                                 |
| [**INFORMAZIONI SUL \_ LIVELLO DI ESECUZIONE DEL CONTESTO DI \_ \_ \_ ATTIVAZIONE**](/windows/desktop/api/Winnt/ns-winnt-activation_context_run_level_information)                 | Usato dalla [**funzione QueryActCtxW.**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)<br/> **Windows Server 2003 e Windows XP:** Questa struttura non è disponibile.<br/>                                                                                                                                                                                                                                    |
| [**ELEMENTO COMPATIBILITY \_ CONTEXT \_**](/windows/desktop/api/Winnt/ns-winnt-compatibility_context_element)                                         | Usato dalla funzione [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) come parte della struttura [**ACTIVATION CONTEXT COMPATIBILITY \_ \_ \_ INFORMATION.**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information) <br/> **Windows Server 2008 e versioni precedenti e Windows Vista e versioni precedenti:** Questa struttura non è disponibile. È disponibile a partire da Windows Server 2008 R2 e Windows 7.<br/> |
| [**INFORMAZIONI SULLA \_ COMPATIBILITÀ \_ DEL CONTESTO DI \_ ATTIVAZIONE**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information)          | Usato dalla [**funzione QueryActCtxW.**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)<br/> **Windows Server 2008 e versioni precedenti e Windows Vista e versioni precedenti:** Questa struttura non è disponibile. È disponibile a partire da Windows Server 2008 R2 e Windows 7.<br/>                                                                                                                                   |



 

Nella tabella seguente sono elencate le enumerazioni del contesto di attivazione.

| Enumerazione                                                                       | Descrizione                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LIVELLO DI ESECUZIONE RICHIESTO \_ \_ \_ ACTCTX**](/windows/desktop/api/Winnt/ne-winnt-actctx_requested_run_level)               | Descrive il livello di esecuzione richiesto del contesto di attivazione. **Windows Server 2003 e Windows XP:** Questa enumerazione non è disponibile.<br/>                                                                                                      |
| [**TIPO DI ELEMENTO \_ DI \_ COMPATIBILITÀ ACTCTX \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_compatibility_element_type) | Descrive l'elemento compatibility nel manifesto dell'applicazione. **Windows Server 2008 e versioni precedenti e Windows Vista e versioni precedenti:** Questa enumerazione non è disponibile. È disponibile a partire da Windows Server 2008 R2 e Windows 7.<br/> |



 

 

