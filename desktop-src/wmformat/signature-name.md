---
title: Signature_Name
description: "\\_L'attributo Nome firma contiene il nome nel certificato usato per firmare il file. Questo attributo è valido solo se l'attributo Is \\_ Trusted è impostato su True."
ms.assetid: 3f3ab10c-731b-4075-8f73-3c2e62e010b9
keywords:
- Signature_Name windows Media Format
topic_type:
- apiref
api_name:
- Signature_Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bff0516353468733ef5c834d51dddc7bbc85e322d98b82929e092913bc375a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845852"
---
# <a name="signature_name"></a>Nome \_ della firma

**\_ L'attributo Nome** firma contiene il nome nel certificato usato per firmare il file. Questo attributo è valido solo se [**l'attributo Is \_ Trusted**](is-trusted.md) è impostato su True.

## <a name="global-constant"></a>Costante globale

g \_ wszWMSignature \_ Name

## <a name="data-type"></a>Tipo di dati

**STRINGA DI TIPO WMT \_ \_**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene usato per un singolo flusso, verrà considerato come metadati personalizzati e non trasmetterà il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




