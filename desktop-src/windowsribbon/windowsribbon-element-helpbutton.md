---
title: Elemento HelpButton
description: Rappresenta il controllo Pulsante ? .
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- Elemento HelpButton nella barra multifunzione di Windows
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f34f04133b7628cce01ac0ce2808923b4f6bbdb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442842"
---
# <a name="helpbutton-element"></a>Elemento HelpButton

Rappresenta il [controllo Pulsante ?](windowsribbon-controls-helpbutton.md) .

## <a name="usage"></a>Utilizzo

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Type</th>
<th>Obbligatoria</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per [**ogni ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).

Avvia una finestra di dialogo della Guida dell'applicazione quando si fa clic su .

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup di base necessario per implementare un controllo Pulsante [? della barra](windowsribbon-controls-helpbutton.md) multifunzione.

Questa sezione di codice illustra la **dichiarazione del comando HelpButton.**


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



Questa sezione di codice mostra la dichiarazione **del controllo HelpButton.**


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a>Informazioni sull'elemento

* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** Sì



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Pulsante ?](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





