---
title: VBRPeak
description: L'attributo VBRPeak contiene la velocità in bit momentanea più elevata in un flusso con codifica VBR (Variable Bit Rate).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- VBRPeak windows Media Format
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9163e64aa3d309af8fd35626b7a4c0397ba4c949213ef351c1ac73ee9575a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704841"
---
# <a name="vbrpeak"></a>VBRPeak

**L'attributo VBRPeak** contiene la velocità in bit momentanea più elevata in un flusso con codifica VBR (Variable Bit Rate).

## <a name="global-constant"></a>Costante globale

g \_ wszVBRPeak

## <a name="data-type"></a>Tipo di dati

**DWORD \_ DI \_ TIPO WMT**

## <a name="remarks"></a>Commenti

Quando si accede **all'interfaccia IWMHeaderInfo3** dell'oggetto writer, è possibile aggiungere o modificare questo valore. In altri oggetti (editor di metadati, lettore e lettore sincrono), questo valore è di sola lettura.

Il writer scrive automaticamente un **valore VBRPeak** per ogni flusso VBR.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




