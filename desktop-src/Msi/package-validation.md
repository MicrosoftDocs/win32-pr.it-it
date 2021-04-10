---
description: Prima di tentare di installare il pacchetto per la prima volta, è consigliabile eseguire la convalida su ogni pacchetto di installazione nuovo o appena modificato.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Convalida del pacchetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880725"
---
# <a name="package-validation"></a>Convalida del pacchetto

Prima di tentare di installare il pacchetto per la prima volta, è consigliabile eseguire la convalida su ogni pacchetto di installazione nuovo o appena modificato.

La convalida del pacchetto include i tre processi seguenti:

-   [Convalida interna](internal-validation.md)
-   [Convalida del pool di stringhe](string-pool-validation.md)
-   [Analizzatori di coerenza interni-CIEM](internal-consistency-evaluators-ices.md)

I moduli merge devono essere convalidati tramite il metodo descritto in [convalida dei moduli unione](validating-merge-modules.md).

Evalcom2.dll fornisce un oggetto COM che implementa le operazioni di convalida per i pacchetti di installazione e i moduli unione. L'oggetto Main implementa le interfacce per i programmi C/C++. Per altre informazioni, vedere [automazione della convalida](validation-automation.md).

 

 



