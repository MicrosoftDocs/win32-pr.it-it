---
description: Ogni proprietà in una classe di visualizzazione deve avere un qualificatore di matrice di stringhe denominato PropertySources.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Qualificatore PropertySources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308840"
---
# <a name="propertysources-qualifier"></a><span data-ttu-id="ebcb2-103">Qualificatore PropertySources</span><span class="sxs-lookup"><span data-stu-id="ebcb2-103">PropertySources Qualifier</span></span>

<span data-ttu-id="ebcb2-104">Ogni proprietà in una classe di visualizzazione deve avere un qualificatore di matrice di stringhe denominato **PropertySources**.</span><span class="sxs-lookup"><span data-stu-id="ebcb2-104">Every property in a view class must have a string array qualifier called **PropertySources**.</span></span> <span data-ttu-id="ebcb2-105">Il qualificatore **PropertySources** contiene il nome della proprietà o delle proprietà della classe di origine da cui questa proprietà della classe di visualizzazione Ottiene i dati.</span><span class="sxs-lookup"><span data-stu-id="ebcb2-105">The **PropertySources** qualifier contains the name of the source class property or properties from which this view class property gets data.</span></span> <span data-ttu-id="ebcb2-106">L'ordine dei valori in questa matrice corrisponde all'ordine delle classi di origine definite per il [qualificatore ViewSources](viewsources-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="ebcb2-106">The order of the values in this array correspond to the order of the source classes defined for the [ViewSources qualifier](viewsources-qualifier.md).</span></span> <span data-ttu-id="ebcb2-107">Nell'esempio seguente viene illustrato come definire una proprietà per una classe di visualizzazione Unione che rappresenta l'Unione della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) da due computer diversi:</span><span class="sxs-lookup"><span data-stu-id="ebcb2-107">The following example shows how to define a property for a union view class that is the union of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class from two different computers:</span></span>


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



<span data-ttu-id="ebcb2-108">La prima proprietà **DeviceID** corrisponde alla proprietà **DeviceID** della classe nella prima query di origine.</span><span class="sxs-lookup"><span data-stu-id="ebcb2-108">The first **DeviceID** property corresponds to the **DeviceID** property from the class in the first source query.</span></span> <span data-ttu-id="ebcb2-109">La seconda proprietà **DeviceID** è la proprietà **DeviceID** della classe nella seconda query di origine.</span><span class="sxs-lookup"><span data-stu-id="ebcb2-109">The second **DeviceID** property is the **DeviceID** property from the class in the second source query.</span></span>

<span data-ttu-id="ebcb2-110">Quando si definiscono le proprietà per le classi di visualizzazione join, è necessario definire una proprietà di visualizzazione separata per ognuna delle proprietà della classe di origine, a meno che le proprietà della classe di origine non siano le basi della classe di visualizzazione join.</span><span class="sxs-lookup"><span data-stu-id="ebcb2-110">When defining properties for join view classes, you must define a separate view property for each of the source class properties unless the source class properties are the basis of the join view class.</span></span> <span data-ttu-id="ebcb2-111">Nell'esempio seguente vengono create proprietà in una classe di visualizzazione join su proprietà simili dalla classe di origine della [**\_ stampante Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e dalla classe di origine [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) :</span><span class="sxs-lookup"><span data-stu-id="ebcb2-111">The following example creates properties in a join view class on similar properties from the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) source class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) source class:</span></span>


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



<span data-ttu-id="ebcb2-112">Se le due classi di origine vengono unite in join da una proprietà comune, è possibile definire solo una singola proprietà della classe di visualizzazione, perché il valore di entrambe le proprietà della classe di origine è sempre lo stesso.</span><span class="sxs-lookup"><span data-stu-id="ebcb2-112">If the two source classes are being joined by a common property, you can only define a single view class property because the value of both source class properties is always the same.</span></span> <span data-ttu-id="ebcb2-113">Nell'esempio seguente viene illustrato come unire in join la classe [**\_ Printer Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e la [**\_ PrinterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) mediante un valore di proprietà comune:</span><span class="sxs-lookup"><span data-stu-id="ebcb2-113">The following example shows how to join the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) by a common property value:</span></span>


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a><span data-ttu-id="ebcb2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebcb2-114">Requirements</span></span>



| <span data-ttu-id="ebcb2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebcb2-115">Requirement</span></span> | <span data-ttu-id="ebcb2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ebcb2-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ebcb2-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebcb2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ebcb2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebcb2-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ebcb2-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebcb2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ebcb2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebcb2-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebcb2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebcb2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebcb2-122">**Qualificatori specifici del provider di visualizzazione**</span><span class="sxs-lookup"><span data-stu-id="ebcb2-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

