---
description: Windows Le funzioni del programma di installazione che restituiscono dati in una posizione di memoria fornita dall'utente non devono essere chiamate con null come valore per il puntatore.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Passaggio di null a funzioni Windows installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6964716479d7e64cc9aa70d7e49acc8fe78dd3343298826e011f6d72b4df1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627664"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a>Passaggio di null come argomento delle funzioni del Windows installer

Windows Le funzioni del programma di installazione che restituiscono dati in una posizione di memoria fornita dall'utente non devono essere chiamate con null come valore per il puntatore. Queste funzioni restituiscono una stringa o restituiscono dati come puntatori integer, ma restituiscono valori incoerenti quando si passa null come valore per l'argomento di output.

Non passare Null come valore dell'argomento di output per una delle funzioni seguenti:

[**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



