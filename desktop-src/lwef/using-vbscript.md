---
title: Uso di VBScript
description: Uso di VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691ed6bf520c83e4b679bb174274abb984eaa2f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221558"
---
# <a name="using-vbscript"></a><span data-ttu-id="0c1e2-103">Uso di VBScript</span><span class="sxs-lookup"><span data-stu-id="0c1e2-103">Using VBScript</span></span>

<span data-ttu-id="0c1e2-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0c1e2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0c1e2-105">VBScript è un linguaggio di programmazione incluso in Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0c1e2-105">VBScript is a programming language included with Microsoft Internet Explorer.</span></span> <span data-ttu-id="0c1e2-106">Per gli altri browser, rivolgersi al fornitore del supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="0c1e2-106">For other browsers, contact your vendor about support.</span></span> <span data-ttu-id="0c1e2-107">È consigliabile usare VBScript 2,0 (o versione successiva) con Agent.</span><span class="sxs-lookup"><span data-stu-id="0c1e2-107">VBScript 2.0 (or later) is recommended for use with Agent.</span></span> <span data-ttu-id="0c1e2-108">Sebbene le versioni precedenti di VBScript possano funzionare con Agent, non hanno determinate funzioni che è possibile usare.</span><span class="sxs-lookup"><span data-stu-id="0c1e2-108">Although earlier versions of VBScript may work with Agent, they lack certain functions that you may want to use.</span></span> <span data-ttu-id="0c1e2-109">È possibile scaricare VBScript 2,0 e ottenere ulteriori informazioni su VBScript nel sito di download Microsoft e nel sito Microsoft VBScript.</span><span class="sxs-lookup"><span data-stu-id="0c1e2-109">You can download VBScript 2.0 and obtain further information on VBScript at the Microsoft Downloads site and the Microsoft VBScript site.</span></span>

<span data-ttu-id="0c1e2-110">Per programmare Microsoft Agent da VBScript, usare il codice HTML</span><span class="sxs-lookup"><span data-stu-id="0c1e2-110">To program Microsoft Agent from VBScript, use the HTML</span></span> <SCRIPT> <span data-ttu-id="0c1e2-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span><span class="sxs-lookup"><span data-stu-id="0c1e2-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span></span>

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

<span data-ttu-id="0c1e2-112">Per gli eventi, includere il nome del controllo seguito dal nome dell'evento e da eventuali parametri:</span><span class="sxs-lookup"><span data-stu-id="0c1e2-112">For events, include the name of the control followed by the name of the event and any parameters:</span></span>

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

<span data-ttu-id="0c1e2-113">È anche possibile specificare un gestore eventi usando il</span><span class="sxs-lookup"><span data-stu-id="0c1e2-113">You can also specify an event handler using the</span></span> <SCRIPT> <span data-ttu-id="0c1e2-114">tag's **For...Event** syntax:</span><span class="sxs-lookup"><span data-stu-id="0c1e2-114">tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

<span data-ttu-id="0c1e2-115">Sebbene Microsoft Internet Explorer supporti questa seconda sintassi, non tutti i browser lo fanno.</span><span class="sxs-lookup"><span data-stu-id="0c1e2-115">Although Microsoft Internet Explorer supports this latter syntax, not all browsers do.</span></span> <span data-ttu-id="0c1e2-116">Per compatibilità, usare solo la sintassi precedente per gli eventi.</span><span class="sxs-lookup"><span data-stu-id="0c1e2-116">For compatibility, use only the former syntax for events.</span></span>

<span data-ttu-id="0c1e2-117">Con VBScript (2,0 o versione successiva), è possibile verificare se Microsoft Agent è installato provando a creare l'oggetto e verificare se esiste.</span><span class="sxs-lookup"><span data-stu-id="0c1e2-117">With VBScript (2.0 or later), you can verify whether Microsoft Agent is installed by trying to create the object and checking to see if it exists.</span></span> <span data-ttu-id="0c1e2-118">Nell'esempio seguente viene illustrato come verificare la presenza del controllo agente senza attivare un download automatico del controllo (come avviene se è stato incluso un <OBJECT> tag per il controllo nella pagina):</span><span class="sxs-lookup"><span data-stu-id="0c1e2-118">The following sample demonstrates how to check for the Agent control without triggering an auto-download of the control (as would happen if you included an <OBJECT> tag for the control on the page):</span></span>

``` syntax
<!-- WARNING - This code requires VBScript 2.0.
It will always fail to detect the Agent control
in VbScript 1.x, because CreateObject doesn't work.
-->

<SCRIPT LANGUAGE=VBSCRIPT>
If HaveAgent() Then
      'Microsoft Agent control was found.
document.write "<H2 align=center>Found</H2>"
Else
      'Microsoft Agent control was not found.
document.write "<H2 align=center>Not Found</H2>"
End If

Function HaveAgent()
' This procedure attempts to create an Agent Control object.
' If it succeeds, it returns True.
'    This means the control is available on the client.
' If it fails, it returns False.
'    This means the control hasn't been installed on the client.

   Dim agent
   HaveAgent = False
   On Error Resume Next
   Set agent = CreateObject("Agent.Control.1")
   HaveAgent = IsObject(agent)

End Function

</SCRIPT>
```

 

 




