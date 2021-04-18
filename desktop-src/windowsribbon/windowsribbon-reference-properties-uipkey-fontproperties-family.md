---
title: UI_PKEY_FontProperties_Family
description: Identifica la \_ proprietà della \_ famiglia FontProperties pkey dell'interfaccia utente \_ .
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7183e51105a397f14154639512ca11f7c03d44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299883"
---
# <a name="ui_pkey_fontproperties_family"></a><span data-ttu-id="0811e-103">Interfaccia \_ utente \_ pkey \_ famiglia FontProperties</span><span class="sxs-lookup"><span data-stu-id="0811e-103">UI\_PKEY\_FontProperties\_Family</span></span>

<span data-ttu-id="0811e-104">Identifica la \_ proprietà della \_ famiglia FontProperties pkey dell'interfaccia utente \_ .</span><span class="sxs-lookup"><span data-stu-id="0811e-104">Identifies the UI\_PKEY\_FontProperties\_Family property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="0811e-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="0811e-105">Remarks</span></span>

<span data-ttu-id="0811e-106">Interfaccia utente \_ pkey \_ FontProperties la \_ famiglia viene utilizzata da un'applicazione per eseguire una query sul valore della raccolta a discesa della **famiglia di caratteri** .</span><span class="sxs-lookup"><span data-stu-id="0811e-106">UI\_PKEY\_FontProperties\_Family is used by an application to query the value of the **Font family** drop-down gallery.</span></span>

<span data-ttu-id="0811e-107">Il valore della \_ famiglia pkey FontProperties di interfaccia utente \_ \_ corrisponde a un nome di [famiglie di caratteri GDI Windows](../gdi/font-families.md) recuperato con la [funzione EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) o [EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span><span class="sxs-lookup"><span data-stu-id="0811e-107">The value of UI\_PKEY\_FontProperties\_Family matches a [Windows GDI Font Families](../gdi/font-families.md) name retrieved with the [EnumFontFamilies function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) or [EnumFontFamiliesEx function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span></span>

<span data-ttu-id="0811e-108">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="0811e-108">The default value is an empty string.</span></span>

<span data-ttu-id="0811e-109">Se viene fornita una stringa vuota per il valore per l'interfaccia utente \_ pkey \_ FontProperties \_ Family, la selezione del tipo di carattere viene deselezionata.</span><span class="sxs-lookup"><span data-stu-id="0811e-109">If an empty string is supplied for the value for UI\_PKEY\_FontProperties\_Family, then the font selection is cleared.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0811e-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0811e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0811e-111">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="0811e-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="0811e-112">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="0811e-112">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 