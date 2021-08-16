---
description: Una regola business consente a un'applicazione di usare la logica in fase di esecuzione per qualificare le autorizzazioni concesse al client.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Regole business
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54260fc6c7dd56137b3065a07f0dcccf9df1c4d21add4b9e7f0cfa79b0300e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783627"
---
# <a name="business-rules"></a>Regole business

Una regola business consente a un'applicazione di usare la logica in fase di esecuzione per qualificare le autorizzazioni concesse al client.

Una regola business è uno script scritto nel linguaggio di programmazione Visual Basic Scripting Edition (VBScript) o scritto usando il software di sviluppo Microsoft JScript associato a un [**oggetto IAzTask.**](/windows/desktop/api/Azroles/nn-azroles-iaztask) Quando un'applicazione controlla l'accesso per un'operazione, Gestione autorizzazioni controlla innanzitutto se il client corrente ha accesso a tutte le attività che contengono tale operazione ma che non sono associate alle regole business. Se l'accesso non viene concesso in questo modo, Gestione autorizzazioni esegue gli script delle regole business associati a qualsiasi attività che contiene l'operazione.

Un'applicazione passa informazioni a uno script della regola business come coppia di matrici che rappresentano i nomi e i valori dei parametri. Lo script ha accesso a questi parametri tramite un [**oggetto AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) creato durante l'esecuzione dello script.

Uno script della regola business non può essere assegnato a un'attività contenuta in un ambito delegato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Qualifica dell'accesso con la logica di business in C++](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



