---
title: Uso di VBScript
description: Uso di VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bc64419af4d8dc47de5a2393fcf5cb259374ed
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881013"
---
# <a name="using-vbscript"></a>Uso di VBScript

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

VBScript è un linguaggio di programmazione incluso in Microsoft Internet Explorer. Per altri browser, contattare il fornitore per assistenza. È consigliabile usare VBScript 2.0 (o versione successiva) con Agent. Anche se le versioni precedenti di VBScript possono funzionare con Agent, non dispongono di alcune funzioni che è possibile usare. È possibile scaricare VBScript 2.0 e ottenere altre informazioni su VBScript nel sito download Microsoft e nel sito Microsoft VBScript.

Per programmare Microsoft Agent da VBScript, usare i tag HTML &lt; &gt; SCRIPT. Per accedere all'interfaccia di programmazione, usare il nome del controllo assegnato nel tag OBJECT, seguito dall'oggetto secondario (se presente), dal nome del metodo o della proprietà ed eventuali parametri o valori supportati dal metodo o dalla &lt; &gt; proprietà:

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

Per gli eventi, includere il nome del controllo seguito dal nome dell'evento ed eventuali parametri:

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

È anche possibile specificare un gestore eventi usando &lt; &gt; for... del tag **SCRIPT. Sintassi** dell'evento:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Anche se Microsoft Internet Explorer supporta questa seconda sintassi, non tutti i browser lo supportano. Per compatibilità, usare solo la sintassi precedente per gli eventi.

Con VBScript (2.0 o versione successiva), è possibile verificare se Microsoft Agent è installato provando a creare l'oggetto e verificando se esiste. L'esempio seguente illustra come verificare la presenza del controllo Agent senza attivare un download automatico del controllo (come accade se si includesse un tag OBJECT per il controllo &lt; &gt; nella pagina):

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

 

 




