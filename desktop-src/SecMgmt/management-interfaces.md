---
description: Elenca le interfacce fornite dal motore degli allegati.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Interfacce di gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6adc6cbaa24be46508e2a4f72181c96d4ccb65e589fdad95808c65a57262b73b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894328"
---
# <a name="security-management-interfaces"></a>Interfacce di gestione della sicurezza

Questa sezione contiene pagine di riferimento per i gruppi di interfacce seguenti:

-   [Interfacce del motore di allegati](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a>Interfacce del motore di allegati



| Interfaccia                                                            | Descrizione                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | Recupera i dati di configurazione e di analisi relativi a un servizio di sicurezza specificato dagli snap-in Di configurazione della sicurezza. Gli snap-in Di configurazione della sicurezza espongono questa interfaccia, che le estensioni degli snap-in degli allegati chiamano per eseguire query sulla configurazione o sulle informazioni di analisi.                                                 |
| [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | Recupera le informazioni di analisi o di configurazione modificate da uno snap-in degli allegati. Gli snap-in Di configurazione della sicurezza chiama questa interfaccia per recuperare le informazioni modificate dall'estensione dello snap-in degli allegati. Lo snap-in Configurazione sicurezza archivia quindi questi dati in modo appropriato nel database di sicurezza. |



 

Per altre informazioni sulle interfacce COM che devono essere implementate dalle estensioni snap-in, vedere la Microsoft Management Console [documentazione.](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page)

 

 
