---
title: Utilizzo di oggetti COM in pagine Active Server
description: È possibile creare script per oggetti COM in applicazioni di Active Server Pages (ASP).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328636"
---
# <a name="using-com-objects-in-active-server-pages"></a>Utilizzo di oggetti COM in pagine Active Server

È possibile creare script per oggetti COM in applicazioni di Active Server Pages (ASP). A tale scopo, è innanzitutto necessario creare un'istanza dell'oggetto utilizzando il tag OBJECT oppure chiamando il metodo CreateObject dell'oggetto ASP server. Una volta creato un oggetto COM, è possibile utilizzarlo negli script successivi della pagina ASP.

Con ASP è possibile utilizzare molti tipi diversi di motori di scripting, ciascuno dei quali supporta un linguaggio di scripting diverso. ASP viene fornita con i motori di script VBScript e JScript. È anche possibile collegare motori di scripting sviluppati da altre società per supportare linguaggi quali PerlScript, PScript, Python e altri.

Se non si imposta il linguaggio di scripting per una pagina ASP, VBScript è il valore predefinito. Per specificare un linguaggio di script diverso da VBScript, includere una riga come la seguente nella parte superiore di ogni pagina ASP:

``` syntax
<%@ LANGUAGE=JScript %>
 
```

Per utilizzare un oggetto COM in una pagina ASP, è innanzitutto necessario creare un'istanza di tale oggetto. A tale scopo, usare il tag OBJECT e specificare il valore "SERVER" per l'attributo RUNAt, come illustrato nell'esempio seguente. Per impostazione predefinita, il tag OBJECT crea un'istanza dell'oggetto nel client. L'impostazione dell'attributo RUNAt sul SERVER comporta la creazione dell'oggetto nel server. L'oggetto deve essere eseguito nel server per poter essere utilizzato da ASP.

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

È inoltre possibile creare un'istanza di un oggetto COM in una pagina ASP chiamando il metodo CreateObject dell'oggetto server ASP. L'utilizzo di server. CreateObject è più lento della creazione dell'oggetto utilizzando un tag OBJECT, ma è leggermente più leggibile perché specifica l'identificatore a livello di codice anziché l'identificatore di classe dell'oggetto COM. L'oggetto server è esposto da ASP e non è necessario crearlo. Negli esempi seguenti viene illustrato come chiamare il metodo Server. CreateObject. Il primo esempio è VBScript:

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

La chiamata a CreateObject è più lenta rispetto all'uso del tag OBJECT per creare un oggetto COM. Nelle applicazioni in cui le prestazioni sono critiche è necessario usare il tag OBJECT.

Una volta creata un'istanza dell'oggetto COM, è possibile utilizzarla negli script. Questa operazione è illustrata nell'esempio VBScript seguente, che imposta il valore della proprietà Border dell'oggetto COM.

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di script con oggetti COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




