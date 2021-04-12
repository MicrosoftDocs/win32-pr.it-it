---
description: Una regola business consente a un'applicazione di usare la logica in fase di esecuzione per qualificare le autorizzazioni concesse al client.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Regole business
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234334"
---
# <a name="business-rules"></a>Regole business

Una regola business consente a un'applicazione di usare la logica in fase di esecuzione per qualificare le autorizzazioni concesse al client.

Una regola business è uno script scritto nel linguaggio di programmazione Visual Basic Scripting Edition (VBScript) o scritto utilizzando il software di sviluppo Microsoft JScript associato a un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) . Quando un'applicazione controlla l'accesso per un'operazione, gestione autorizzazioni verifica innanzitutto se il client corrente ha accesso a tutte le attività che contengono tale operazione ma non associate alle regole business. Se l'accesso non viene concesso in questo modo, gestione autorizzazioni esegue gli script della regola business associati a qualsiasi attività che contiene l'operazione.

Un'applicazione passa informazioni a uno script della regola business come una coppia di matrici che rappresentano i nomi e i valori dei parametri. Lo script può accedere a questi parametri tramite un oggetto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) creato durante l'esecuzione dello script.

Uno script della regola business non può essere assegnato a un'attività contenuta in un ambito delegato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Qualificazione dell'accesso con la logica di business in C++](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



