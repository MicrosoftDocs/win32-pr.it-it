---
title: Signature_Name
description: L' \_ attributo Signature Name contiene il nome del certificato usato per firmare il file. Questo attributo è valido solo se l' \_ attributo è attendibile è impostato su true.
ms.assetid: 3f3ab10c-731b-4075-8f73-3c2e62e010b9
keywords:
- Signature_Name formato Windows Media
topic_type:
- apiref
api_name:
- Signature_Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af378671a570dd9ffc58021081b3925d3dca21af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718484"
---
# <a name="signature_name"></a>\_Nome firma

L'attributo **Signature \_ Name** contiene il nome del certificato usato per firmare il file. Questo attributo è valido solo se l'attributo [**è \_ attendibile**](is-trusted.md) è impostato su true.

## <a name="global-constant"></a>Costante globale

\_nome wszWMSignature \_ g

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




