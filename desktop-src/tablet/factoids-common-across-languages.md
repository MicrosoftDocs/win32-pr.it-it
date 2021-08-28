---
description: Alcuni factoid descrivono l'input comune a tutti i riconoscitori linguistici e non devono avere formati diversi per lingue diverse. Nella tabella seguente sono elencati i factoid comuni in tutti i linguaggi.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factoid comuni tra lingue diverse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407a82c72367d0123414f72b083b1d3416cfc958
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473877"
---
# <a name="factoids-common-across-languages"></a>Factoid comuni tra lingue diverse

Alcuni factoid descrivono l'input comune a tutti i riconoscitori linguistici e non devono avere formati diversi per lingue diverse. Nella tabella seguente sono elencati i factoid comuni in tutti i linguaggi.




| Factoid | Definizione | Esempio | 
|---------|------------|----------|
| <strong>Cifre</strong> | Imposta la distorsione per una singola cifra. Il riconoscitore è orientato a restituire solo cifre singole quando questo factoid è impostato.<br /> | 0-9<br /> | 
| <strong>Posta elettronica</strong> | Imposta la distorsione per un indirizzo di posta elettronica.<br /> | someone@example.com<br /> | 
| <strong>Web</strong> | Imposta la distorsione per vari formati di URL.<br /><blockquote>[!Note]<br />Le impostazioni predefinite per il riconoscimento includono il factoid <strong>Web.</strong> Per questo, è possibile che non si noti una grande differenza tra il factoid <strong>Web</strong> e l'impostazione predefinita. Tuttavia, il factoid <strong>Web</strong> consente di eliminare gli spazi tra le parole in un URL.</blockquote><br /> | http: \\ microsoft.net<br /> https://microsoft.us/<br /> https: \\ www.microsoft.au \<br />https://microsoft.com<br /> www.microsoft_world.com<br /> www.microsoft.us \<br /> http: \\www.microsoft.com\myfile.htm<br /> http: \\www.microsoft.com\myfile.html<br /> http: \\ www.microsoft.com\myfile.asp<br /> http: \\ www.microsoft.uk<br /> http: \\ www.microsoft.info<br /> www.microsoft.biz<br /> | 
| <strong>Default</strong> | Restituisce il riconoscitore alle impostazioni predefinite.<br /> | L'impostazione predefinita per i factoid per le lingue occidentali include il dizionario di sistema, il dizionario utente, varie punteggiatura e i factoid <strong>Web</strong> e <strong>Number.</strong><br /> L'impostazione predefinita per i factoid per le lingue dell'Asia orientale include tutti i caratteri supportati dal sistema di riconoscimento.<br /> | 
| <strong>Nessuno</strong> | Disabilita tutti i factoid, i dizionari e il modello linguistico.<br /> | Questo factoid deve essere usato solo quando non si vuole che il sistema di riconoscimento usi regole grammaticali o dizionari, incluso il dizionario di sistema. Questo factoid è utile per l'input di stringhe casuali, ad esempio codici prodotto. Non usare il flag Coerce con questo factoid.<br /> | 




 

 

 




