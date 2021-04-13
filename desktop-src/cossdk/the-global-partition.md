---
description: Partizione globale
ms.assetid: db11e6f5-0a3d-44ce-9a51-90d7e2b80981
title: Partizione globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc218067bbf7170a1c2df6f306b6dfe5787ac2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483861"
---
# <a name="the-global-partition"></a>Partizione globale

Oltre alle partizioni e ai set di partizioni definiti dall'amministratore, esiste una partizione speciale in ogni computer denominato *partizione globale*. Quando si installa COM+, viene creata automaticamente una partizione globale. La partizione globale è progettata per contenere applicazioni a livello di sistema che devono essere accessibili a tutti gli utenti in un server o nel dominio. L'installazione di un'applicazione nella partizione globale elimina la necessità di installare una copia dell'applicazione nel set di partizioni di ogni singolo utente.

Se il set di partizioni di un utente non include un'applicazione specifica a cui l'utente sta tentando di accedere, ma tale applicazione viene installata nella partizione globale, l'applicazione viene attivata dalla partizione globale. In questo caso, tuttavia, tutti i componenti dell'applicazione installati nella partizione globale devono essere contrassegnati come componenti pubblici, non privati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Partizioni predefinite](default-partitions.md)
</dt> <dt>

[Partizioni locali](local-partitions.md)
</dt> <dt>

[Proprietà partizione](partition-properties.md)
</dt> <dt>

[Partizioni e Active Directory](partitions-and-active-directory.md)
</dt> </dl>

 

 



