---
description: La struttura COMMCONFIG definisce la configurazione di una risorsa di comunicazione, seriale o altro.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Configurazione delle risorse di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01cd85a60eabc3cf6adcbdb0e05d2fbdc662442029044a5ac67d9a37bc073d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918321"
---
# <a name="communications-resource-configuration"></a>Configurazione delle risorse di comunicazione

La [**struttura COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) definisce la configurazione di una risorsa di comunicazione, seriale o altro. Il formato della struttura varia a seconda del tipo di risorsa di comunicazione (sottotipo provider). I primi membri della struttura sono comuni a tutte le risorse di comunicazione. sono definiti membri aggiuntivi per sottotipi di provider specifici. Provider di servizi specifici possono estendere anche **la struttura COMMCONFIG.**

Un'applicazione può ottenere e impostare la configurazione di una risorsa di comunicazione usando le [**funzioni GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) [**e SetCommConfig.**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) Quando viene aperta, una risorsa di comunicazione viene inizializzata usando la configurazione predefinita per il sottotipo del provider. Per ottenere e impostare la configurazione predefinita per un sottotipo di provider, usare le [**funzioni GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) [**e SetDefaultCommConfig.**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)

Per richiedere informazioni di configurazione all'utente, usare la [**funzione CommConfigDialog.**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) Questa funzione visualizza una finestra di dialogo definita dal provider di servizi e compila una [**struttura COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) in base all'input dell'utente.

 

 



