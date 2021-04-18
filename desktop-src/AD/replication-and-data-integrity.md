---
title: Replica e integrità dei dati
description: Active Directory Domain Services fornire aggiornamenti multimaster.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo, replica e integrità dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297721"
---
# <a name="replication-and-data-integrity"></a>Replica e integrità dei dati

Active Directory Domain Services fornire *aggiornamenti multimaster*. L'aggiornamento multimaster indica che tutte le repliche complete di una determinata partizione sono scrivibili (le repliche parziali nei server di catalogo globale non sono scrivibili). L'aggiornamento multimaster indica che gli aggiornamenti non vengono bloccati anche quando alcune repliche sono inutilizzabili. Il server di Active Directory propaga le modifiche dalla replica aggiornata a tutte le altre repliche. La replica è automatica e trasparente.

Per ulteriori informazioni, vedere gli argomenti seguenti.

-   [Il modello di replica in Active Directory Domain Services](replication-model-in-active-directory-domain-services.md)
-   [Comportamento della replica in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md)
-   [Rilevamento ed evitare la latenza di replica](detecting-and-avoiding-replication-latency.md)

 

 




