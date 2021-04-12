---
description: .
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sicurezza (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbaaa6b34463e04f5870082e5c693462f4e19fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234330"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Sicurezza (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

A partire da Windows Internet Explorer 7, Windows Internet Explorer viene eseguito in un contesto di sicurezza denominato *modalità protetta* quando gli utenti eseguono il sistema operativo Windows Vista o una versione successiva. Questa modalità esegue Internet Explorer in un'impostazione con privilegi inferiori rispetto a un'applicazione utente standard, in modo che alcune funzionalità siano limitate, in particolare i controlli ActiveX e determinati tipi di plug-in. Per ulteriori informazioni sulla modalità protetta in Internet Explorer e sul relativo effetto sulla compatibilità, vedere [informazioni e utilizzo in modalità protetta di Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in MSDN Library.

Per impostazione predefinita, Windows Internet Explorer 8 Abilita anche protezione esecuzione programmi, che consente alle applicazioni di evitare l'esecuzione di codice arbitrario negli attacchi online. Tuttavia, alcuni componenti aggiuntivi potrebbero non utilizzare questa funzionalità di sicurezza (ad esempio, eventuali componenti aggiuntivi non progettati per eseguire solo codice che si trova in memoria che è stato contrassegnato come eseguibile, ad esempio le applicazioni compilate utilizzando una versione precedente del framework ATL (ActiveX Template Library).

Internet Explorer 8 protegge anche gli utenti da potenziali vulnerabilità della sicurezza che usano gli script. Ad esempio, non è possibile passare da un URL in una zona meno attendibile a un URL in una zona più attendibile, ad eccezione dell'interazione esplicita dell'utente. Non è inoltre possibile nascondere alcuni elementi dell'interfaccia utente del browser (ad esempio la barra degli indirizzi) in una zona non attendibile (Internet).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiornamenti della progettazione che incidono sulla compatibilità tra browser](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
