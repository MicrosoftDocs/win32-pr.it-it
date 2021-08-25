---
title: Uso di oggetti COM in Active Server pagine
description: È possibile creare script per oggetti COM in applicazioni ASP (Active Server Pages).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8ba1bbdd0729a8893b1c28d1a2347fc5ddea04c8d0de4e1ea413e765ab8df4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896200"
---
# <a name="using-com-objects-in-active-server-pages"></a>Uso di oggetti COM in Active Server pagine

È possibile creare script per oggetti COM in applicazioni ASP (Active Server Pages). A tale scopo, è innanzitutto necessario creare un'istanza dell'oggetto usando il tag OBJECT o chiamando il metodo CreateObject dell'oggetto Server ASP. Dopo aver creato un oggetto COM, è possibile usarlo negli script successivi nella pagina ASP.

Con ASP è possibile usare molti tipi diversi di motori di scripting, ognuno dei quali supporta un linguaggio di scripting diverso. ASP viene fornito con VBScript e JScript di scripting. È anche possibile collegare motori di scripting sviluppati da altre società per supportare linguaggi come PerlScript, PScript, Python e altri.

Se non si imposta il linguaggio di scripting per una pagina ASP, vbscript è il linguaggio predefinito. Per specificare un linguaggio di scripting diverso da VBScript, includere una riga simile alla seguente nella parte superiore di ogni pagina ASP:

``` syntax
<%@ LANGUAGE=JScript %>
 
```

Per utilizzare un oggetto COM in una pagina ASP, è innanzitutto necessario creare un'istanza di tale oggetto. A tale scopo, usare il tag OBJECT e specificare il valore "SERVER" per l'attributo RUNAT, come illustrato nell'esempio seguente. Per impostazione predefinita, il tag OBJECT crea un'istanza dell'oggetto nel client. Se si imposta l'attributo RUNAT su SERVER, l'oggetto viene creato nel server. L'oggetto deve essere eseguito nel server per poter essere utilizzato da ASP.

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

È anche possibile creare un'istanza di un oggetto COM in una pagina ASP chiamando il metodo CreateObject dell'oggetto Server ASP. L'uso di Server.CreateObject è più lento rispetto alla creazione dell'oggetto con un tag OBJECT, ma è leggermente più leggibile perché specifica l'identificatore a livello di codice anziché l'identificatore di classe dell'oggetto COM. L'oggetto Server viene esposto da ASP e non deve essere creato. Negli esempi seguenti viene illustrato come chiamare Server.CreateObject. Il primo esempio è VBScript:

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

L'esempio successivo è JScript:

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

La chiamata a CreateObject è più lenta rispetto all'uso del tag OBJECT per creare un oggetto COM. Nelle applicazioni in cui le prestazioni sono critiche, è consigliabile usare il tag OBJECT.

Dopo aver creato un'istanza dell'oggetto COM, è possibile usarla negli script. Questa operazione è illustrata nell'esempio VBScript seguente, che imposta il valore della proprietà Border dell'oggetto COM.

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di script con oggetti COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




