---
description: Informazioni sulle definizioni dei parametri in un documento PrintCapabilities. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Definizioni dei parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dad2f596592efddfafe97b32660d92bb67b6097012fe9599f89ce0e63526f72e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034059"
---
# <a name="parameter-definitions"></a>Definizioni dei parametri

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

In questa sezione vengono descritte le definizioni dei parametri pubblici che possono essere visualizzate in un documento PrintCapabilities.

I parametri vengono usati per descrivere un intervallo accettabile di valori, anziché un'enumerazione discreta di valori.

## <a name="parameterdef"></a>ParameterDef

Per un riepilogo del tipo di elemento ParameterDef, vedere la [sezione ParameterDef.](parameterdef.md)

Per altre informazioni sull'interazione tra elementi ParameterDef ed elementi ParameterInit, vedere la sezione Elementi ParameterDef e [ParameterInit.](./parameterdef-and-parameterinit-elements.md)

Gli elementi ParameterDef definiti nelle parole chiave dello schema di stampa devono essere completamente definiti in un documento PrintCapabilities.

## <a name="parameterref"></a>ParameterRef

Per un riepilogo del tipo di elemento ParameterRef, vedere la [sezione ParameterRef.](parameterref.md)

Una parola chiave dell'elemento configurabile dall'utente può contenere un riferimento a un parametro. Gli elementi ParameterRef vengono specificati come figlio di un elemento ScoredProperty Per altre informazioni, vedere la [sezione Elementi di riferimento dei](parameter-reference-elements.md) parametri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
