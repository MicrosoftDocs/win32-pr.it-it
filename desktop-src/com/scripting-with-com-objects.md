---
title: Creazione di script con oggetti COM
description: Creazione di script con oggetti COM
ms.assetid: d99a561b-67dc-4fc9-adfa-cd7350eb16ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2b00380a14db2d254675a5826b61f262e8cfe8
ms.sourcegitcommit: 8c981a2f4149b4a9d605ffb71fefda8d82bc696e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/24/2019
ms.locfileid: "103717665"
---
# <a name="scripting-with-com-objects"></a>Creazione di script con oggetti COM

Un *linguaggio di scripting* è un linguaggio di programmazione analizzato in fase di esecuzione da un *motore di script*, un componente che converte gli script scritti in tale lingua nel codice del computer. Ogni motore di script converte un linguaggio di scripting specifico. Un *host di scripting* è un'applicazione, ad esempio una Web browser, che ospita un motore di script per l'esecuzione di script. Se l'host di scripting supporta COM, è possibile scrivere script che utilizzano oggetti COM. Negli argomenti seguenti vengono descritti gli host di scripting che supportano gli oggetti COM, i linguaggi di scripting comuni e le modalità di conversione tra i linguaggi di scripting.

Un linguaggio di scripting è diverso da un linguaggio compilato perché viene convertito in codice macchina in fase di esecuzione. Ciò significa che ogni volta che si esegue uno script, il motore di scripting analizza prima di tutto il codice e quindi lo esegue. Al contrario, i linguaggi compilati, ad esempio C++, vengono convertiti in codice macchina una volta, durante la compilazione. Quando si esegue un'applicazione compilata, il sistema operativo esegue semplicemente il codice precompilato.

Poiché un motore di scripting deve analizzare uno script ogni volta che viene eseguito, i linguaggi di scripting sono in genere più lenti e meno efficienti rispetto alle controparti precompilate. Il vantaggio degli script, tuttavia, è facile da scrivere e gestire. I linguaggi di scripting sono in genere più semplici rispetto ai linguaggi precompilati e quando uno script viene modificato non è necessario ricompilarlo. Per le applicazioni leggere e in rapida evoluzione, ad esempio le pagine Web, i linguaggi di scripting sono ideali.

Sono disponibili diversi ambienti host in cui è possibile scrivere script che utilizzano oggetti COM, come descritto di seguito:

-   [Incorporamento di oggetti COM in pagine Web](embedding-com-objects-in-web-pages.md)
-   [Utilizzo di oggetti COM in pagine Active Server](using-com-objects-in-active-server-pages.md)
-   [Utilizzo di oggetti COM in Windows script host](using-com-objects-in-windows-script-host.md)
-   [Creazione di script per oggetti COM in applicazioni personalizzate](scripting-com-objects-in-custom-applications.md)

In ogni ambiente host indicato in precedenza, un motore di script analizza ed esegue lo script. Poiché il motore di ogni linguaggio di scripting è un componente separato, è possibile aggiungere un nuovo linguaggio di scripting a un ambiente aggiungendo un nuovo motore.

I linguaggi di scripting usati più di frequente sono:

-   Microsoft Visual Basic Scripting Edition (VBScript), un sottoinsieme di Visual Basic.
-   JavaScript, il linguaggio di scripting Netscape, in precedenza noto come LiveScript.
-   Software di sviluppo Microsoft JScript, l'implementazione Microsoft della specifica del linguaggio ECMA 262.

Microsoft fornisce motori di script per JScript e VBScript. Altre società software forniscono motori di script ActiveX per linguaggi come PerlScript, PScript, Python e altri.

Per ulteriori informazioni, vedere la [specifica del linguaggio ECMA 262](https://www.ecma-international.org/publications/standards/Ecma-262.htm).

Si noti che la maggior parte dei linguaggi di scripting, ad esempio VBScript e JScript, non può accedere o modificare i file. Questa impossibilità impedisce allo script di modificare i dati nei computer client. Gli oggetti COM, tuttavia, non hanno limitazioni di questo tipo. Una volta scaricati e installati nei computer client, è possibile eseguire qualsiasi azione standard dell'applicazione. Pertanto, gli utenti devono scaricare ed eseguire i controlli ActiveX solo da origini attendibili.

Per informazioni sulla conversione tra i linguaggi di scripting, vedere gli argomenti seguenti:

-   [Conversione in VBScript](translating-to-vbscript.md)
-   [Conversione in JScript](translating-to-jscript.md)
-   [Conversione in JavaScript](translating-to-javascript.md)

 

 




