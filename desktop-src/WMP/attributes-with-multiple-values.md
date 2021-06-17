---
title: Attributi con più valori (Windows Media Player SDK)
description: Informazioni sugli attributi con più valori in Windows Media Player SDK. Alcuni attributi dell'elemento multimediale possono avere più valori.
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player,attributi per elementi multimediali
- Windows Media Player a oggetti, attributi per elementi multimediali
- modello a oggetti,attributi per elementi multimediali
- Windows Media Player Mobile, attributi per elementi multimediali
- Windows Media Player controllo ActiveX, attributi per elementi multimediali
- Windows Media Player controllo ActiveX mobile, attributi per elementi multimediali
- Controllo ActiveX,attributi per elementi multimediali
- Windows Media Player,attributi per elementi multimediali
- libreria,attributi per elementi multimediali
- attributi,più valori
- più valori di attributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16baf4bab47dc972ec7b043980dccb0f2aadd57
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262603"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a>Attributi con più valori (Windows Media Player SDK)

Alcuni attributi dell'elemento multimediale possono avere più valori. Ad esempio, gli **attributi Author**, **WM/Composer** e **WM/Genre** possono avere più di un valore. Il tipo di dati di tali attributi è **stringa multivalore**.

In Windows Media Player la libreria visualizza più valori in un singolo campo, separandoli con punti e virgola. Tuttavia, ogni valore è in realtà un attributo separato nell'elemento di Windows Media.

È possibile scrivere codice che determinerà se un determinato attributo ha più valori e quindi recupera tutti questi valori. È necessario usare *Media*. **getItemInfoByType**. Se si usa l'oggetto *Media*. **metodo getItemInfo** per recuperare un attributo multivalore, si recupererà solo il primo valore.

L'esempio finale [nell'argomento Reading Attribute Values](reading-attribute-values.md) (Lettura dei valori degli attributi) illustra l'uso di *Media*. **getAttributeCountByType** e *Media*. **Metodi getItemInfoByType** per recuperare più valori per un determinato attributo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi dell'elemento multimediale**](media-item-attributes.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Lettura dei valori degli attributi da un CD o dvd**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




