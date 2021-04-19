---
description: Elenca le interfacce fornite dal motore degli allegati.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Interfacce di gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316642"
---
# <a name="security-management-interfaces"></a>Interfacce di gestione della sicurezza

Questa sezione contiene le pagine di riferimento per i gruppi di interfacce seguenti:

-   [Interfacce del motore allegati](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a>Interfacce del motore allegati



| Interfaccia                                                            | Descrizione                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | Recupera i dati di configurazione e analisi relativi a un servizio di sicurezza specificato dagli snap-in di configurazione della sicurezza. Gli snap-in configurazione di sicurezza espongono questa interfaccia, che consente alle estensioni degli snap-in di eseguire una chiamata alle informazioni di configurazione o di analisi.                                                 |
| [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | Recupera le informazioni di configurazione o analisi modificate da uno snap-in allegato. Gli snap-in configurazione di sicurezza chiamano questa interfaccia per recuperare le informazioni modificate dall'estensione dello snap-in allegati. Lo snap-in Configurazione sicurezza archivia quindi questi dati in modo appropriato nel database di sicurezza. |



 

Per ulteriori informazioni sulle interfacce COM che devono essere implementate dalle estensioni di snap-in, vedere la documentazione di [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

 

 
