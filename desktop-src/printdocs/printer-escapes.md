---
description: Il carattere di escape della stampante fornito da Windows a 16 bit ha consentito l'accesso alle funzionalità speciali del dispositivo.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Caratteri di escape della stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232135"
---
# <a name="printer-escapes"></a>Caratteri di escape della stampante

Il carattere di escape della stampante fornito da Windows a 16 bit ha consentito l'accesso alle funzionalità speciali del dispositivo. La maggior parte di questi caratteri di escape è obsoleta, ma ne sono stati forniti alcuni per semplificare il porting delle applicazioni basate su Windows a 16 bit. GDI supporta un set completo di funzioni di percorso che le applicazioni possono usare al posto degli escape per tracciare i percorsi su qualsiasi dispositivo. Per un elenco di funzioni che sostituiscono alcuni caratteri di escape, vedere la funzione [**escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) .

Delle 64 di escape della stampante originale, è possibile usare solo **QUERYESCSUPPORT** e **PassThrough** .

È disponibile anche una funzione di escape estesa denominata [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Questa funzione consente alle applicazioni di accedere alle funzionalità di un dispositivo specifico non direttamente disponibili tramite GDI.

 

 



