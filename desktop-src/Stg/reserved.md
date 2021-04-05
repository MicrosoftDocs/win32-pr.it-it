---
title: Riservato
description: Il valore del tipo di dati DWORD è riservato per un utilizzo futuro.
ms.assetid: 3b49c064-43d0-4e76-b199-c2f6d1c153d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d791debea3835ec1b2fb1fc9d48df7c92114e44e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856997"
---
# <a name="reserved"></a>Riservato

Il valore del tipo di dati **DWORD** è riservato per un utilizzo futuro. I writer dei set di proprietà devono impostare questo valore su 1; i reader dei set di proprietà devono assicurarsi che il valore sia almeno pari a 1. Un'eccezione a questa linea guida è che, per [i set di proprietà DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md), questo valore può essere 2.

 

 




