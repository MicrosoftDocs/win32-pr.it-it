---
title: VBRPeak
description: L'attributo VBRPeak contiene la velocità in bit più elevata del momento in un flusso codificato a velocità in bit variabile (VBR).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- VBRPeak Windows Media Format
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045832"
---
# <a name="vbrpeak"></a>VBRPeak

L'attributo **VBRPeak** contiene la velocità in bit più elevata del momento in un flusso codificato a velocità in bit variabile (VBR).

## <a name="global-constant"></a>Costante globale

g \_ wszVBRPeak

## <a name="data-type"></a>Tipo di dati

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Commenti

Quando si accede all'interfaccia **IWMHeaderInfo3** dell'oggetto writer, è possibile aggiungere o modificare questo valore. In altri oggetti (editor di metadati, lettore e lettore sincrono), questo valore è di sola lettura.

Il writer scrive automaticamente un valore **VBRPeak** per ogni flusso VBR.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




