---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Definizioni dei parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5a71bfc5a5111a826b5d221ff1436ecf921dd2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234571"
---
# <a name="parameter-definitions"></a>Definizioni dei parametri

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

In questa sezione vengono descritte le definizioni dei parametri pubblici che possono essere visualizzate in un documento PrintCapabilities.

I parametri vengono usati per descrivere un intervallo di valori accettabile, anziché un'enumerazione discreta di valori.

## <a name="parameterdef"></a>ParameterDef

Per un riepilogo del tipo di elemento ParameterDef, vedere la sezione [ParameterDef](parameterdef.md) .

Per altre informazioni sull'interazione tra gli elementi ParameterDef e gli elementi ParameterInit, vedere la sezione [elementi ParameterDef e ParameterInit](./parameterdef-and-parameterinit-elements.md) .

Gli elementi ParameterDef definiti nelle parole chiave Print Schema devono essere definiti completamente in un documento PrintCapabilities.

## <a name="parameterref"></a>ParameterRef

Per un riepilogo del tipo di elemento ParameterRef, vedere la sezione [ParameterRef](parameterref.md) .

Una parola chiave dell'elemento configurabile dall'utente può contenere un riferimento a un parametro. Gli elementi ParameterRef vengono specificati come elementi figlio di un elemento ScoredProperty per altre informazioni. vedere la sezione [elementi di riferimento ai parametri](parameter-reference-elements.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
