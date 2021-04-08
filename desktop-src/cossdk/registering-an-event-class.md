---
description: In modo che i sottoscrittori possano trovare una classe di evento e sottoscriverla, le classi di evento devono essere registrate nel catalogo COM+.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Registrazione di una classe di evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748290"
---
# <a name="registering-an-event-class"></a>Registrazione di una classe di evento

In modo che i sottoscrittori possano trovare una classe di evento e sottoscriverla, le classi di evento devono essere registrate nel catalogo COM+. COM+ richiede una libreria dei tipi che descrive le interfacce e i metodi degli eventi in modo che sia possibile trovare una corrispondenza corretta e connettere i sottoscrittori e i Publisher. La libreria dei tipi deve risiedere in o essere accompagnata da una DLL con registrazione automatica.

È possibile utilizzare lo strumento di amministrazione Servizi componenti o le funzioni amministrative COM+ per registrare una classe di evento nel catalogo COM+.

**Per registrare una classe di evento con lo strumento di amministrazione Servizi componenti**

1.  Creare una nuova applicazione COM+.

2.  Aprire la cartella dell'applicazione e selezionare **componenti**.

3.  Scegliere **Nuovo** dal menu **Azione**. È anche possibile selezionare la cartella **componenti** , fare clic con il pulsante destro del mouse, scegliere **nuovo**, quindi fare clic su **componente**.

4.  Fare clic su **installa nuove classi di evento**.

5.  Immettere il percorso della DLL del componente della classe di evento.

6.  Fare clic su **OK**.

La classe di evento è registrata nel catalogo COM+ e può essere individuata dai sottoscrittori interessati a ottenere le informazioni fornite dalla classe di evento. Per informazioni su come registrare la classe di evento usando le interfacce amministrative COM+, vedere [**ICOMAdminCatalog:: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di una sottoscrizione](registering-a-subscription.md)
</dt> </dl>

 

 



