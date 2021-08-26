---
description: È consigliabile eseguire la convalida in ogni pacchetto di installazione nuovo o appena modificato prima di provare a installare il pacchetto per la prima volta.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Convalida dei pacchetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2fb8fe877f68a1c787458e7703fb59f035031fc68bba1d75f24e86851aac7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074851"
---
# <a name="package-validation"></a>Convalida dei pacchetti

È consigliabile eseguire la convalida in ogni pacchetto di installazione nuovo o appena modificato prima di provare a installare il pacchetto per la prima volta.

La convalida dei pacchetti include i tre processi seguenti:

-   [Convalida interna](internal-validation.md)
-   [Convalida del pool di stringhe](string-pool-validation.md)
-   [Analizzatori di coerenza interna - ICE](internal-consistency-evaluators-ices.md)

I moduli unione devono essere convalidati usando il metodo descritto in [Convalida dei moduli unione](validating-merge-modules.md).

Evalcom2.dll fornisce un oggetto COM che implementa le operazioni di convalida per i pacchetti di installazione e i moduli unione. L'oggetto principale implementa le interfacce per i programmi C/C++. Per altre informazioni, vedere [Automazione convalida](validation-automation.md).

 

 



