---
title: Attributi con più valori (Windows Media Player SDK)
description: Attributi con più valori
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Media Player di Windows, attributi per elementi multimediali
- Modello a oggetti di Windows Media Player, attributi per elementi multimediali
- modello a oggetti, attributi per elementi multimediali
- Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX di Windows Media Player, attributi per elementi multimediali
- Controllo ActiveX Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX, attributi per elementi multimediali
- Windows Media Player Library, attributi per elementi multimediali
- libreria, attributi per elementi multimediali
- attributi, più valori
- più valori di attributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad93c4025d09a234b1834a32e4ca3789bcaa4a35
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400154"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a>Attributi con più valori (Windows Media Player SDK)

Alcuni attributi dell'elemento multimediale possono avere più valori. Ad esempio, gli attributi **Author**, **WM/Composer** e **WM/genre** possono avere più di un valore. Il tipo di dati di tali attributi è costituito da una **stringa multivalore**.

In Windows Media Player la libreria Visualizza più valori in un singolo campo, separando i valori con un punto e virgola. Tuttavia, ogni valore è effettivamente un attributo separato nell'elemento multimediale di Windows.

È possibile scrivere codice per determinare se un attributo specificato dispone di più valori e quindi recuperare tutti questi valori. È necessario utilizzare *supporti*. **getItemInfoByType**. Se si usa il *supporto*. metodo **GetItemInfo** per recuperare un attributo multivalore, si recupererà solo il primo valore.

Nell'esempio finale nell'argomento [Reading attribute values](reading-attribute-values.md) viene illustrato l'utilizzo del *supporto*. **getAttributeCountByType** e *supporti*. metodi **getItemInfoByType** per recuperare più valori per un attributo specificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi elemento multimediale**](media-item-attributes.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Lettura di valori di attributo da un CD o DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




