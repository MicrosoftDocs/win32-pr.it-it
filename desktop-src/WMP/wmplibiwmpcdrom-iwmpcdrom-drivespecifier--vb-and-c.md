---
title: Proprietà driveSpecifier di IWMPCdrom
description: La proprietà driveSpecifier ottiene la lettera dell'unità CD o DVD.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- Finestra delle proprietà di driveSpecifier Media Player
- Proprietà di driveSpecifier Media Player Windows, interfaccia IWMPCdrom
- Interfaccia IWMPCdrom Windows Media Player, proprietà driveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a6c439523d90824da708700d48274f5a2e5ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329676"
---
# <a name="iwmpcdromdrivespecifier-property"></a><span data-ttu-id="2b991-106">IWMPCdrom::d proprietà riveSpecifier</span><span class="sxs-lookup"><span data-stu-id="2b991-106">IWMPCdrom::driveSpecifier property</span></span>

<span data-ttu-id="2b991-107">La proprietà **driveSpecifier** ottiene la lettera dell'unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="2b991-107">The **driveSpecifier** property gets the CD or DVD drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b991-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b991-108">Syntax</span></span>


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a><span data-ttu-id="2b991-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2b991-109">Property value</span></span>

<span data-ttu-id="2b991-110">**System. String** che corrisponde alla lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="2b991-110">A **System.String** that is the drive letter.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b991-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b991-111">Remarks</span></span>

<span data-ttu-id="2b991-112">In genere, le unità DVD possono riprodurre supporti CD, ma le unità CD non possono riprodurre supporti DVD.</span><span class="sxs-lookup"><span data-stu-id="2b991-112">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="2b991-113">Questa proprietà ottiene una lettera di unità per un indice di unità in base zero nell'intervallo recuperato utilizzando **IWMPCdromCollection. Count**.</span><span class="sxs-lookup"><span data-stu-id="2b991-113">This property gets a drive letter for a zero-based drive index within the range retrieved using **IWMPCdromCollection.count**.</span></span> <span data-ttu-id="2b991-114">Il valore recuperato assume il formato *x*:, dove *x* rappresenta la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="2b991-114">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="2b991-115">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="2b991-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="2b991-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2b991-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2b991-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="2b991-117">Examples</span></span>

<span data-ttu-id="2b991-118">Nell'esempio seguente viene usato **driveSpecifier** per compilare una stringa che contiene un elenco di unità CD e DVD disponibili e visualizza tale stringa in una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="2b991-118">The following example uses **driveSpecifier** to build a string that contains a list of available CD and DVD drives and displays that string in a message box.</span></span> <span data-ttu-id="2b991-119">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="2b991-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
```





## <a name="requirements"></a><span data-ttu-id="2b991-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b991-120">Requirements</span></span>



| <span data-ttu-id="2b991-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b991-121">Requirement</span></span> | <span data-ttu-id="2b991-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2b991-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b991-123">Versione</span><span class="sxs-lookup"><span data-stu-id="2b991-123">Version</span></span><br/>   | <span data-ttu-id="2b991-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2b991-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2b991-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2b991-125">Namespace</span></span><br/> | <span data-ttu-id="2b991-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2b991-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2b991-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="2b991-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2b991-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2b991-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b991-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b991-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b991-130">**Interfaccia IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2b991-130">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b991-131">**IWMPCdromCollection. Count (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2b991-131">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b991-132">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2b991-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b991-133">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2b991-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





