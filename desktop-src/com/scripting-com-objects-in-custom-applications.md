---
title: Creazione di script per oggetti COM in applicazioni personalizzate
description: Creazione di script per oggetti COM in applicazioni personalizzate
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221319"
---
# <a name="scripting-com-objects-in-custom-applications"></a>Creazione di script per oggetti COM in applicazioni personalizzate

Microsoft offre diversi ambienti per la creazione di script per gli oggetti COM: pagine Active Server, Windows script host e così via. I fornitori di software indipendenti (ISV) possono anche concedere in licenza i motori di script Microsoft per l'uso nelle applicazioni. Ad esempio, un ISV che crea un elaboratore di testo potrebbe voler aggiungere un linguaggio macro all'applicazione in modo che gli utenti possano automatizzare le attività semplici. Grazie alla gestione delle licenze di un motore di script, l'ISV può utilizzare un linguaggio come VBScript o JScript come linguaggio macro dell'applicazione.

Oltre alla gestione delle licenze dei motori di scripting VBScript e JScript, gli ISV possono scrivere i propri motori di script ActiveX. Questi motori di scripting possono quindi essere inseriti in qualsiasi ambiente host che supporti lo standard del motore di scripting ActiveX. Ad esempio, un ISV potrebbe scrivere un motore di script PerlScript e installarlo in un server ASP, consentendo così al server ASP di elaborare gli script PerlScript.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di script con oggetti COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




