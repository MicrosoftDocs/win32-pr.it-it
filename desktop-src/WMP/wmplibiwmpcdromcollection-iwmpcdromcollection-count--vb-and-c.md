---
title: IWMPCdromCollection-proprietà conteggio
description: La proprietà Count ottiene il numero di unità CD e DVD disponibili nel sistema.
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- conteggio delle proprietà di Windows Media Player
- Proprietà Count Media Player Windows, interfaccia IWMPCdromCollection
- Interfaccia IWMPCdromCollection Windows Media Player, proprietà Count
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329652"
---
# <a name="iwmpcdromcollectioncount-property"></a><span data-ttu-id="562e9-106">Proprietà IWMPCdromCollection:: count</span><span class="sxs-lookup"><span data-stu-id="562e9-106">IWMPCdromCollection::count property</span></span>

<span data-ttu-id="562e9-107">La proprietà **count** ottiene il numero di unità CD e DVD disponibili nel sistema.</span><span class="sxs-lookup"><span data-stu-id="562e9-107">The **count** property gets the number of available CD and DVD drives on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="562e9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="562e9-108">Syntax</span></span>


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="562e9-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="562e9-109">Property value</span></span>

<span data-ttu-id="562e9-110">**System. Int32** che rappresenta il numero di unità disponibili.</span><span class="sxs-lookup"><span data-stu-id="562e9-110">A **System.Int32** that is the count of available drives.</span></span>

## <a name="remarks"></a><span data-ttu-id="562e9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="562e9-111">Remarks</span></span>

<span data-ttu-id="562e9-112">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="562e9-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="562e9-113">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="562e9-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="562e9-114">Le unità DVD sono conteggiate esattamente come le unità CD.</span><span class="sxs-lookup"><span data-stu-id="562e9-114">DVD drives are counted exactly like CD drives.</span></span> <span data-ttu-id="562e9-115">Tuttavia, il controllo ActiveX di Windows Media Player supporta solo la funzionalità DVD per Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="562e9-115">However, the Windows Media Player ActiveX control only supports DVD functionality for Windows XP or later.</span></span> <span data-ttu-id="562e9-116">In genere, le unità DVD possono riprodurre supporti CD, ma le unità CD non possono riprodurre supporti DVD.</span><span class="sxs-lookup"><span data-stu-id="562e9-116">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

## <a name="examples"></a><span data-ttu-id="562e9-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="562e9-117">Examples</span></span>

<span data-ttu-id="562e9-118">Nell'esempio seguente viene utilizzato Count per visualizzare il numero di unità CD e DVD disponibili in una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="562e9-118">The following example uses count to display the number of available CD and DVD drives in a message box.</span></span> <span data-ttu-id="562e9-119">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="562e9-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a><span data-ttu-id="562e9-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="562e9-120">Requirements</span></span>



| <span data-ttu-id="562e9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="562e9-121">Requirement</span></span> | <span data-ttu-id="562e9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="562e9-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="562e9-123">Versione</span><span class="sxs-lookup"><span data-stu-id="562e9-123">Version</span></span><br/>   | <span data-ttu-id="562e9-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="562e9-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="562e9-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="562e9-125">Namespace</span></span><br/> | <span data-ttu-id="562e9-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="562e9-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="562e9-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="562e9-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="562e9-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="562e9-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="562e9-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="562e9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562e9-130">**Interfaccia IWMPCdromCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="562e9-130">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="562e9-131">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="562e9-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="562e9-132">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="562e9-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





