---
description: Considerazioni sulla sicurezza di COM+ CRM
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Considerazioni sulla sicurezza di COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1052f9e8cf4f23dd80e2b4706b7e13c0f39a2aedd9b9a985da2d41101118467d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638731"
---
# <a name="com-crm-security-considerations"></a>Considerazioni sulla sicurezza di COM+ CRM

Un file di log crm può contenere informazioni riservate che devono essere protette. Per questo motivo, se l'applicazione server è in esecuzione con un'identità diversa da Interactive User al momento della creazione del file di log di CRM, il file di log crm è protetto solo per tale utente. Questa funzionalità è disponibile solo nel file system NTFS. Se successivamente l'identità dell'applicazione server viene modificata, le informazioni di sicurezza per il file di log crm non vengono modificate automaticamente. Può essere modificato manualmente usando gli strumenti di amministrazione Windows esistenti. L'alternativa consiste semplicemente nell'eliminare il file di log crm quando si trova in uno stato pulito (previsto dopo un arresto controllato dell'applicazione server).

Nel normale funzionamento, COM+ crea il componente compensatore CRM e chiama [**l'interfaccia ICrmCompensator.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) Tuttavia, un utente con privilegi per creare CRM Compensator può chiamare **l'interfaccia ICrmCompensator** in momenti non appropriati, causando eventualmente problemi di sicurezza del sistema. Per proteggere da questi problemi di sicurezza, l'amministratore di sistema può usare la sicurezza basata sui ruoli per limitare il componente CRM Compensator solo alle identità delle applicazioni server in cui viene eseguito. Se il componente è in esecuzione in un'applicazione libreria, verranno incluse tutte le identità delle applicazioni server.

> [!Note]  
> A partire da Windows Server 2003, per impedire l'attivazione dall'esterno dell'applicazione server, è possibile garantire ulteriormente un sistema più sicuro contrassegnando il componente CRM Compensator come privato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi alla compensazione Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



