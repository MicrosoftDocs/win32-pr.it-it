---
description: Sicurezza (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sicurezza (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f320f4cb561079380e19a969eba95f3f6b321fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116229"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Sicurezza (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

A partire da Windows Internet Explorer 7, Windows Internet Explorer viene eseguito  in un contesto di sicurezza denominato Modalità protetta quando gli utenti la eseguono nel sistema operativo Windows Vista o in una versione successiva. Questa modalità viene Internet Explorer in un'impostazione con privilegi inferiori rispetto a un'applicazione utente standard, quindi alcune funzionalità sono limitate, in particolare i controlli ActiveX e alcuni tipi di plug-in. Per altre informazioni sulla modalità protetta in Internet Explorer e sul relativo impatto sulla compatibilità, vedere Understanding [and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in MSDN Library.

Per impostazione predefinita, Windows Internet Explorer 8 abilita anche Protezione esecuzione programmi, che consente alle applicazioni di evitare l'esecuzione di codice arbitrario negli attacchi online. Tuttavia, alcuni componenti aggiuntivi potrebbero non usare questa funzionalità di sicurezza( ad esempio, tutti i componenti aggiuntivi che non sono progettati per eseguire solo il codice che si trova in memoria che è stato contrassegnato in modo specifico come eseguibile, ad esempio le applicazioni compilate usando una versione precedente del framework ATL (ActiveX Template Library).

Internet Explorer 8 protegge anche gli utenti da potenziali vulnerabilità della sicurezza che usano script. Ad esempio, non è possibile passare da un URL in un'area meno attendibile a un URL in un'area più attendibile, tranne tramite l'interazione esplicita dell'utente. Non è inoltre possibile nascondere determinati elementi dell'interfaccia utente del browser, ad esempio la barra degli indirizzi, in un'area non attendibile (Internet).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettare aggiornamenti che influiscono sulla compatibilità tra browser](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
