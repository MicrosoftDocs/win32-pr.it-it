---
description: La struttura COMMCONFIG definisce la configurazione di una risorsa di comunicazione, seriale o in altro modo.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Configurazione delle risorse di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126801"
---
# <a name="communications-resource-configuration"></a>Configurazione delle risorse di comunicazione

La struttura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) definisce la configurazione di una risorsa di comunicazione, seriale o in altro modo. Il formato della struttura varia a seconda del tipo di risorsa di comunicazione (il sottotipo del provider). I primi membri della struttura sono comuni a tutte le risorse di comunicazione; sono definiti membri aggiuntivi per sottotipi di provider specifici. I provider di servizi specifici possono estendere anche la struttura **COMMCONFIG** .

Un'applicazione può ottenere e impostare la configurazione di una risorsa di comunicazione usando le funzioni [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) e [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) . Quando viene aperto, una risorsa di comunicazione viene inizializzata usando la configurazione predefinita per il relativo sottotipo di provider. Per ottenere e impostare la configurazione predefinita per un sottotipo di provider, usare le funzioni [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) e [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .

Per richiedere all'utente le informazioni di configurazione, usare la funzione [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) . Questa funzione Visualizza una finestra di dialogo definita dal provider di servizi e compila una struttura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) in base all'input dell'utente.

 

 



