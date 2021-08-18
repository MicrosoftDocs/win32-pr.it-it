---
description: Sicurezza (Windows 7 e Windows cookbook sulla qualità delle applicazioni di Server 2008 R2)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sicurezza (Windows 7 e Windows cookbook sulla qualità delle applicazioni di Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d392f5bf14997962173b9054baba861003877d851d6bd62a947b15757feec23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994661"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Sicurezza (Windows 7 e Windows cookbook sulla qualità delle applicazioni di Server 2008 R2)

A partire da Windows Internet Explorer 7, Windows Internet Explorer viene eseguito  in un contesto di sicurezza denominato Modalità protetta quando gli utenti la eseguono nel sistema operativo Windows Vista o in una versione successiva. Questa modalità viene Internet Explorer in un'impostazione con privilegi inferiori rispetto a un'applicazione utente standard, quindi alcune funzionalità sono limitate, in particolare i controlli ActiveX e determinati tipi di plug-in. Per altre informazioni sulla modalità protetta in Internet Explorer e sul relativo impatto sulla compatibilità, vedere Understanding [and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in MSDN Library.

Per impostazione predefinita, Windows Internet Explorer 8 abilita anche Protezione esecuzione programmi, che consente alle applicazioni di evitare l'esecuzione di codice arbitrario in attacchi online. Tuttavia, alcuni componenti aggiuntivi potrebbero non usare questa funzionalità di sicurezza, ad esempio i componenti aggiuntivi non progettati per eseguire solo codice che si trova in memoria che è stato contrassegnato in modo specifico come eseguibile, ad esempio applicazioni compilate usando una versione precedente del framework atl (ATL) della libreria di modelli di ActiveX.

Internet Explorer 8 protegge anche gli utenti da potenziali vulnerabilità di sicurezza che usano script. Ad esempio, non è possibile passare da un URL in un'area meno attendibile a un URL in un'area più attendibile, ad eccezione dell'interazione esplicita dell'utente. Non è inoltre possibile nascondere determinati elementi dell'interfaccia utente del browser, ad esempio la barra degli indirizzi, in un'area non attendibile (Internet).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiornamenti della progettazione che influiscono sulla compatibilità tra browser](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
