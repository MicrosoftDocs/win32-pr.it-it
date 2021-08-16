---
title: Creazione di script con oggetti COM
description: Creazione di script con oggetti COM
ms.assetid: d99a561b-67dc-4fc9-adfa-cd7350eb16ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c40d94ddd0316d3a921d5d1ecd4591775700c967008ad801cdd8439a341dd9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918382"
---
# <a name="scripting-with-com-objects"></a>Creazione di script con oggetti COM

Un *linguaggio di scripting* è un linguaggio di programmazione analizzato in fase di esecuzione da un motore di *scripting,* un componente che converte gli script scritti in tale linguaggio in codice macchina. Ogni motore di scripting converte un linguaggio di scripting specifico. Un *host di scripting* è un'applicazione, ad esempio un Web browser, che ospita un motore di scripting per eseguire script. Se l'host di scripting supporta COM, è possibile scrivere script che usano oggetti COM. Negli argomenti seguenti vengono descritti gli host di scripting che supportano oggetti COM, linguaggi di scripting comuni e come eseguire la conversione tra linguaggi di scripting.

Un linguaggio di scripting è diverso da un linguaggio compilato in quanto viene convertito in codice macchina in fase di esecuzione. Ciò significa che ogni volta che si esegue uno script, il motore di scripting analizza prima il codice e quindi lo esegue. Al contrario, i linguaggi compilati, ad esempio C++, vengono convertiti una volta in codice macchina durante la compilazione. Quando si esegue un'applicazione compilata, il sistema operativo esegue semplicemente il codice precompilato.

Poiché un motore di scripting deve eseguire nuovamente l'analisi di uno script ogni volta che viene eseguito, i linguaggi di scripting sono in genere più lenti e meno efficienti rispetto alle controparti precompilate. Il vantaggio degli script, tuttavia, è che sono facili da scrivere e gestire. I linguaggi di scripting sono in genere più semplici rispetto ai linguaggi precompilati e quando uno script cambia, non è necessario ricompilarlo. Per applicazioni leggere e in rapida evoluzione, ad esempio pagine Web, i linguaggi di scripting sono ideali.

Esistono diversi ambienti host in cui è possibile scrivere script che usano oggetti COM, come descritto di seguito:

-   [Incorporamento di oggetti COM nelle pagine Web](embedding-com-objects-in-web-pages.md)
-   [Uso di oggetti COM in Active Server pagine](using-com-objects-in-active-server-pages.md)
-   [Uso di oggetti COM nell'host Windows script](using-com-objects-in-windows-script-host.md)
-   [Scripting di oggetti COM in applicazioni personalizzate](scripting-com-objects-in-custom-applications.md)

In ognuno degli ambienti host indicati in precedenza, un motore di scripting analizza ed esegue lo script. Poiché il motore per ogni linguaggio di scripting è un componente separato, è possibile aggiungere un nuovo linguaggio di scripting a un ambiente aggiungendo un nuovo motore.

I linguaggi di scripting usati più di frequente sono:

-   Microsoft Visual Basic Scripting Edition (VBScript), un subset di Visual Basic.
-   JavaScript, il linguaggio di scripting Netscape, noto in precedenza come LiveScript.
-   Microsoft JScript software di sviluppo, l'implementazione Microsoft della specifica del linguaggio ECMA 262.

Microsoft fornisce motori di scripting per JScript e VBScript. Altre società di software ActiveX motori di scripting per linguaggi come PerlScript, PScript, Python e altri.

Per altre informazioni, vedere la specifica del linguaggio [ECMA 262](https://www.ecma-international.org/publications/standards/Ecma-262.htm).

Si noti che la maggior parte dei linguaggi di scripting, ad esempio VBScript e JScript, non può accedere o modificare i file. Questa inabilità impedisce allo script di modificare i dati nei computer client. Gli oggetti COM, tuttavia, non presentano tali limitazioni. Una volta scaricati e installati nei computer client, possono eseguire qualsiasi azione standard dell'applicazione. Di conseguenza, gli utenti devono solo scaricare ed eseguire ActiveX da origini attendibili.

Per informazioni sulla traduzione tra linguaggi di scripting, vedere gli argomenti seguenti:

-   [Conversione in VBScript](translating-to-vbscript.md)
-   [Traduzione in JScript](translating-to-jscript.md)
-   [Conversione in JavaScript](translating-to-javascript.md)

 

 




