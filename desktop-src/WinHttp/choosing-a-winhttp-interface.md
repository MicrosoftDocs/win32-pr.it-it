---
description: Prima di iniziare a sviluppare un'applicazione di servizi HTTP di Microsoft Windows (WinHTTP), è necessario innanzitutto decidere se utilizzare l'API C/C++ o l'interfaccia COM.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Scelta di un'interfaccia WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313233"
---
# <a name="choosing-a-winhttp-interface"></a>Scelta di un'interfaccia WinHTTP

Prima di iniziare a sviluppare un'applicazione di servizi HTTP di Microsoft Windows (WinHTTP), è necessario innanzitutto decidere se utilizzare l'API C/C++ o l'interfaccia COM. Nella tabella seguente vengono riepilogati i vantaggi e gli svantaggi associati a ognuno di questi approcci.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>API C/C++</th>
<th>Interfaccia COM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vantaggi</td>
<td><ul>
<li>Le risposte possono essere elaborate in blocchi, che risultano più efficienti.</li>
<li>Le operazioni POST possono anche essere elaborate in blocchi, velocizzando il tempo di elaborazione.</li>
<li>Supporto del proxy AutoProxy.</li>
<li>Accesso al set completo di funzionalità di WinHTTP.</li>
<li>I dati binari possono essere facilmente gestiti.</li>
</ul></td>
<td><ul>
<li>La creazione di un'applicazione è semplice e richiede un minor numero di righe di codice rispetto all'API C/C++.</li>
<li>L'interfaccia può essere utilizzata dai linguaggi di scripting.</li>
</ul></td>
</tr>
<tr class="even">
<td>Svantaggi</td>
<td><ul>
<li>L'elaborazione è più complessa.</li>
<li>L'API C/C++ richiede più passaggi rispetto all'interfaccia COM per eseguire le stesse azioni.</li>
<li>La configurazione di una richiesta richiede più codice.</li>
</ul></td>
<td><ul>
<li>L'interfaccia COM non fornisce l'accesso al set completo di funzionalità di WinHTTP.</li>
<li>È difficile gestire i tipi di dati binari in alcuni linguaggi di scripting, ad esempio VBScript e JScript.</li>
<li>L'interfaccia COM non supporta il proxy AutoProxy.</li>
<li>Le applicazioni devono utilizzare il modello di APARTMENT_THREADED COM.</li>
<li>Prima che una risposta possa iniziare a essere elaborata, l'intera risposta deve prima essere ricevuta e memorizzata nel buffer.</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



