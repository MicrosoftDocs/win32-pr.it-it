---
description: Considerazioni sulla sicurezza di COM+ CRM
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Considerazioni sulla sicurezza di COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ababde9f31c0c2655fbf4f0c46b216ca0cbfee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126357"
---
# <a name="com-crm-security-considerations"></a>Considerazioni sulla sicurezza di COM+ CRM

Un file di log CRM potrebbe contenere informazioni riservate che devono essere protette. Per questo motivo, se l'applicazione server viene eseguita con una qualsiasi identità diversa dall'utente interattivo quando viene creato per la prima volta il file di log CRM, il file di log CRM è protetto dalla sicurezza solo per tale utente. Questa funzionalità è disponibile solo nel file system NTFS. Se successivamente si modifica l'identità dell'applicazione server, le informazioni di sicurezza per il file di log CRM non vengono modificate automaticamente. Può essere modificato manualmente usando gli strumenti di amministrazione di Windows esistenti. L'alternativa consiste semplicemente nell'eliminare il file di log CRM quando si trova in uno stato pulito, che è previsto dopo un arresto controllato dell'applicazione server.

Nel normale funzionamento, COM+ crea il componente di compensazione CRM e chiama l'interfaccia [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) . Tuttavia, un utente che dispone dei privilegi per creare il compensatore CRM può chiamare l'interfaccia **ICrmCompensator** in momenti inappropriati, causando possibili problemi di sicurezza del sistema. Per garantire la protezione da questi problemi di sicurezza, l'amministratore di sistema può utilizzare la protezione basata sui ruoli per limitare il componente di compensazione CRM solo alle identità delle applicazioni server in cui è in esecuzione. Se il componente è in esecuzione in un'applicazione di libreria, sono incluse tutte le identità delle applicazioni server.

> [!Note]  
> A partire da Windows Server 2003, per impedire l'attivazione dall'esterno dell'applicazione server, è possibile garantire un sistema più sicuro contrassegnando il componente CRM Compensator come privato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti Gestione risorse di compensazione COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



