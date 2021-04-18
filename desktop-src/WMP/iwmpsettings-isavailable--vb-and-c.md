---
title: IWMPSettings. disavailable (VB e C)
description: La proprietà disavailable (il \_ metodo Get disavailable in C \) ottiene un valore che indica se è possibile eseguire un'azione specificata.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- IWMPSettings. disavailable (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932f0adb325c4c2f9f88e9f80d75ecaecd3ca85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325442"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a><span data-ttu-id="77f29-104">IWMPSettings. disavailable (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="77f29-104">IWMPSettings.isAvailable (VB and C#)</span></span>

<span data-ttu-id="77f29-105">La proprietà **disavailable** (il metodo **get \_ disavailable** in C#) ottiene un valore che indica se è possibile eseguire un'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="77f29-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="77f29-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="77f29-106">Parameters</span></span>

<span data-ttu-id="77f29-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="77f29-107">*bstrItem*</span></span>

<span data-ttu-id="77f29-108">**System. String** che corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="77f29-108">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="77f29-109">Valore</span><span class="sxs-lookup"><span data-stu-id="77f29-109">Value</span></span>              | <span data-ttu-id="77f29-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77f29-110">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77f29-111">avvio automatico</span><span class="sxs-lookup"><span data-stu-id="77f29-111">AutoStart</span></span>          | <span data-ttu-id="77f29-112">Rileva se la proprietà AutoStart può essere impostata in modo da specificare che Windows Media Player avvia automaticamente la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="77f29-112">Discovers whether the autoStart property can be set to specify that Windows Media Player starts playback automatically.</span></span> |
| <span data-ttu-id="77f29-113">Balance</span><span class="sxs-lookup"><span data-stu-id="77f29-113">Balance</span></span>            | <span data-ttu-id="77f29-114">Individua se è possibile utilizzare la proprietà Balance per impostare il bilanciamento dello stereo.</span><span class="sxs-lookup"><span data-stu-id="77f29-114">Discovers whether the balance property can be used to set the stereo balance.</span></span>                                           |
| <span data-ttu-id="77f29-115">BaseURL</span><span class="sxs-lookup"><span data-stu-id="77f29-115">BaseURL</span></span>            | <span data-ttu-id="77f29-116">Rileva se la proprietà baseURL può essere impostata in modo da specificare un URL di base.</span><span class="sxs-lookup"><span data-stu-id="77f29-116">Discovers whether the baseURL property can be set to specify a base URL.</span></span>                                                |
| <span data-ttu-id="77f29-117">DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="77f29-117">DefaultFrame</span></span>       | <span data-ttu-id="77f29-118">Rileva se la proprietà defaultFrame può essere impostata in modo da specificare il frame predefinito.</span><span class="sxs-lookup"><span data-stu-id="77f29-118">Discovers whether the defaultFrame property can be set to specify the default frame.</span></span>                                    |
| <span data-ttu-id="77f29-119">EnableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="77f29-119">EnableErrorDialogs</span></span> | <span data-ttu-id="77f29-120">Rileva se la proprietà enableErrorDialogs può essere impostata in modo da abilitare o disabilitare la visualizzazione delle finestre di dialogo di errore.</span><span class="sxs-lookup"><span data-stu-id="77f29-120">Discovers whether the enableErrorDialogs property can be set to enable or disable displaying error dialog boxes.</span></span>        |
| <span data-ttu-id="77f29-121">GetMode</span><span class="sxs-lookup"><span data-stu-id="77f29-121">GetMode</span></span>            | <span data-ttu-id="77f29-122">Rileva se il metodo GetMode può essere utilizzato per recuperare il ciclo corrente o la modalità shuffle.</span><span class="sxs-lookup"><span data-stu-id="77f29-122">Discovers whether the getMode method can be used to retrieve the current loop or shuffle mode.</span></span>                          |
| <span data-ttu-id="77f29-123">InvokeURLs</span><span class="sxs-lookup"><span data-stu-id="77f29-123">InvokeURLs</span></span>         | <span data-ttu-id="77f29-124">Rileva se la proprietà invokeURLs può essere impostata in modo da specificare se gli eventi URL devono avviare un Web browser.</span><span class="sxs-lookup"><span data-stu-id="77f29-124">Discovers whether the invokeURLs property can be set to specify whether URL events should launch a Web browser.</span></span>         |
| <span data-ttu-id="77f29-125">Disattiva audio</span><span class="sxs-lookup"><span data-stu-id="77f29-125">Mute</span></span>               | <span data-ttu-id="77f29-126">Individua se è possibile impostare la proprietà mute per specificare se l'output audio è on o off.</span><span class="sxs-lookup"><span data-stu-id="77f29-126">Discovers whether the mute property can be set to specify whether the audio output is on or off.</span></span>                        |
| <span data-ttu-id="77f29-127">PlayCount</span><span class="sxs-lookup"><span data-stu-id="77f29-127">PlayCount</span></span>          | <span data-ttu-id="77f29-128">Rileva se la proprietà playCount può essere impostata in modo da specificare il numero di volte in cui un elemento multimediale verrà riprodotto.</span><span class="sxs-lookup"><span data-stu-id="77f29-128">Discovers whether the playCount property can be set to specify the number times a media item will play.</span></span>                 |
| <span data-ttu-id="77f29-129">Tariffa</span><span class="sxs-lookup"><span data-stu-id="77f29-129">Rate</span></span>               | <span data-ttu-id="77f29-130">Individua se è possibile impostare la proprietà rate per controllare la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="77f29-130">Discovers whether the rate property can be set to control the playback rate.</span></span>                                            |
| <span data-ttu-id="77f29-131">SetMode</span><span class="sxs-lookup"><span data-stu-id="77f29-131">SetMode</span></span>            | <span data-ttu-id="77f29-132">Individua se è possibile utilizzare il metodo semode per specificare il ciclo corrente o la modalità shuffle.</span><span class="sxs-lookup"><span data-stu-id="77f29-132">Discovers whether the setMode method can be used to specify the current loop or shuffle mode.</span></span>                           |
| <span data-ttu-id="77f29-133">Volume</span><span class="sxs-lookup"><span data-stu-id="77f29-133">Volume</span></span>             | <span data-ttu-id="77f29-134">Individua se è possibile impostare la proprietà volume per specificare il volume audio.</span><span class="sxs-lookup"><span data-stu-id="77f29-134">Discovers whether the volume property can be set to specify the audio volume.</span></span>                                           |



 

## <a name="property-value"></a><span data-ttu-id="77f29-135">Valore della proprietà</span><span class="sxs-lookup"><span data-stu-id="77f29-135">Property Value</span></span>

<span data-ttu-id="77f29-136">Valore **System. Boolean** che indica se è possibile eseguire l'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="77f29-136">A **System.Boolean** value indicating whether the specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="77f29-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="77f29-137">Remarks</span></span>

<span data-ttu-id="77f29-138">**IWMPSettings. is identico** è una proprietà in Visual Basic che accetta un parametro.</span><span class="sxs-lookup"><span data-stu-id="77f29-138">**IWMPSettings.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="77f29-139">In C# viene indicato come il metodo **IWMPSettings. Get è \_ identico** .</span><span class="sxs-lookup"><span data-stu-id="77f29-139">In C# it is referred to as the **IWMPSettings.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="77f29-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="77f29-140">Examples</span></span>

<span data-ttu-id="77f29-141">Nell'esempio seguente viene testato ogni proprietà **IWMPSettings** utilizzando **la proprietà IsValid** (il metodo **get \_ unavailable** in C#).</span><span class="sxs-lookup"><span data-stu-id="77f29-141">The following example tests each of the **IWMPSettings** properties using the **isAvailable** property (the **get\_isAvailable** method in C#).</span></span> <span data-ttu-id="77f29-142">Il nome della proprietà e il risultato di ogni test vengono visualizzati in una casella di testo a più righe.</span><span class="sxs-lookup"><span data-stu-id="77f29-142">The property name and the result of each test are displayed in a multi-line text box.</span></span> <span data-ttu-id="77f29-143">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="77f29-143">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a><span data-ttu-id="77f29-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77f29-144">Requirements</span></span>



| <span data-ttu-id="77f29-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="77f29-145">Requirement</span></span> | <span data-ttu-id="77f29-146">Valore</span><span class="sxs-lookup"><span data-stu-id="77f29-146">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77f29-147">Versione</span><span class="sxs-lookup"><span data-stu-id="77f29-147">Version</span></span><br/>   | <span data-ttu-id="77f29-148">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="77f29-148">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="77f29-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="77f29-149">Namespace</span></span><br/> | <span data-ttu-id="77f29-150">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="77f29-150">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="77f29-151">Assembly</span><span class="sxs-lookup"><span data-stu-id="77f29-151">Assembly</span></span><br/>  | <dl> <span data-ttu-id="77f29-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="77f29-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77f29-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77f29-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f29-154">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-154">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-155">**IWMPSettings. AutoStart (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-155">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-156">**IWMPSettings. Balance (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-156">**IWMPSettings.balance (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-157">**IWMPSettings. baseURL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-157">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-158">**IWMPSettings. defaultFrame (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-158">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-159">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-159">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-160">**IWMPSettings. getMode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-160">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-161">**IWMPSettings. invokeURLs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-161">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-162">**IWMPSettings. mute (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-162">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-163">**IWMPSettings. playCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-163">**IWMPSettings.playCount (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-164">**IWMPSettings. rate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-164">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-165">**IWMPSettings. semode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-165">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77f29-166">**IWMPSettings. volume (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="77f29-166">**IWMPSettings.volume (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





