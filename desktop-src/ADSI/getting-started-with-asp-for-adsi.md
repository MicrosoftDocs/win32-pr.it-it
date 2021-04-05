---
title: Introduzione con ASP per ADSI
description: È possibile utilizzare ADSI per accedere ai dati della directory utilizzando una pagina ASP. Si tratta di un modo pratico per eseguire le attività di amministrazione e le query da una pagina Web o fornire informazioni ai dipendenti in una rete Intranet.
ms.assetid: 2007257c-6c4e-415e-9ab5-e65d8d9e5dd4
ms.tgt_platform: multiple
keywords:
- ASP ADSI
- ADSI, pagine ASP
- ADSI, ASP Pages, esempio di codice ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5b18093c3817d7a6c3d0224b722f8dd4983c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707420"
---
# <a name="getting-started-with-asp-for-adsi"></a>Introduzione con ASP per ADSI

È possibile utilizzare ADSI per accedere ai dati della directory utilizzando una pagina ASP. Si tratta di un modo pratico per eseguire le attività di amministrazione e le query da una pagina Web o fornire informazioni ai dipendenti in una rete Intranet.

Uno dei vantaggi dell'utilizzo di ADSI con ASP è la possibilità di creare un'esperienza utente più completa, in quanto è possibile utilizzare Visual Basic per creare un'applicazione ADSI e offrirla a un utente tramite una pagina Web standard. Ad esempio, è possibile creare una pagina Web che consente ai dipendenti di immettere il cognome di un dipendente e ottenere un numero di telefono per quel dipendente oppure creare un modulo che consenta ai dipendenti di aggiornare le informazioni personali in un database delle risorse umane della società.

Il codice ASP inizia con "<%" e termina con "% >". È possibile aggiungere il codice ADSI come VBScript o Visual Basic.

Per creare una pagina ASP, è possibile usare un editor di pagine Web, un blocco note o un altro editor di testo o il sistema di sviluppo Microsoft Visual Studio .NET.

Prima di eseguire la pagina ASP, configurare l'applicazione o il server IIS seguendo le istruzioni disponibili in [problemi di autenticazione per ADSI con ASP](authentication-issues-for-adsi-with-asp.md).

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a>Esempio ASP semplice: enumerazione di oggetti in un contenitore

Usando un editor di pagine Web, creare una nuova pagina HTML che accetti il nome distinto di un oggetto contenitore. Immettere l'esempio di codice seguente.


```HTML
<html>
<body>

<form method="POST" action="https://localhost/Enum.asp" ID="Form1">
<p>Distinguished name of container:<input type="text" name="inpContainer" size="100" ID="Text2"></p>
<p><input type="SUBMIT" value="GO" ID="Submit1" NAME="Submit1"></p>
</form>

</body>
</html>
```



In questa pagina è ora possibile accettare un nome di contenitore che viene passato e utilizzare ADSI per enumerare gli oggetti nel contenitore.

Creare una nuova pagina ASP denominata Enum. asp e immettere l'esempio di codice seguente. Salvare questa pagina nella radice del server Web locale.


```VB
<%@ Language=VBScript %>
<%
' Get the inputs.
containerName = Request.Form("inpContainer")
' Validate compName before using.

If Not ("" = containerName) Then
  ' Bind to the object.
  adsPath = "LDAP://" & containerName
  Set comp = GetObject(adsPath)

  ' Write the ADsPath of each of the child objects.
  Response.Write("<p>Enumeration:</p>")
  For Each obj in comp
    Response.Write(obj.ADsPath + "<BR>")
  Next
End If
%>
```



 

 




