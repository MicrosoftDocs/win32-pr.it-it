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
# <a name="using-vbscript"></a>Uso di VBScript

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

VBScript è un linguaggio di programmazione incluso in Microsoft Internet Explorer. Per gli altri browser, rivolgersi al fornitore del supporto tecnico. È consigliabile usare VBScript 2,0 (o versione successiva) con Agent. Sebbene le versioni precedenti di VBScript possano funzionare con Agent, non hanno determinate funzioni che è possibile usare. È possibile scaricare VBScript 2,0 e ottenere ulteriori informazioni su VBScript nel sito di download Microsoft e nel sito Microsoft VBScript.

Per programmare Microsoft Agent da VBScript, usare il codice HTML <SCRIPT> tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

Per gli eventi, includere il nome del controllo seguito dal nome dell'evento e da eventuali parametri:

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

È anche possibile specificare un gestore eventi usando il <SCRIPT> tag's **For...Event** syntax:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Sebbene Microsoft Internet Explorer supporti questa seconda sintassi, non tutti i browser lo fanno. Per compatibilità, usare solo la sintassi precedente per gli eventi.

Con VBScript (2,0 o versione successiva), è possibile verificare se Microsoft Agent è installato provando a creare l'oggetto e verificare se esiste. Nell'esempio seguente viene illustrato come verificare la presenza del controllo agente senza attivare un download automatico del controllo (come avviene se è stato incluso un <OBJECT> tag per il controllo nella pagina):

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

 

 




