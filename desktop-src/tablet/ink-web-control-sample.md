---
description: Questo esempio illustra come creare un controllo abilitato per l'input penna da usare in un Web browser. L'esempio accetta il modulo di attestazione automatica originale e lo trasforma in un controllo inserito in una pagina Web.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Esempio di controllo Web Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101537c4cc7b42181cf8d9ff177a5854c5b84054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306744"
---
# <a name="ink-web-control-sample"></a>Esempio di controllo Web Ink

Questo esempio illustra come creare un controllo abilitato per l'input penna da usare in un Web browser. L'esempio accetta il [modulo di attestazione automatica](auto-claims-form-sample.md) originale e lo trasforma in un controllo inserito in una pagina Web.

Per ulteriori informazioni sull'utilizzo di input penna sul Web, vedere [input penna sul Web](ink-on-the-web.md).

## <a name="modifications-to-the-original-sample-project"></a>Modifiche al progetto di esempio originale

Questo esempio è costituito da una soluzione che include due progetti e un file HTML. Il primo progetto, autoclaims, è un progetto di libreria di controlli Microsoft Visual C \# (un controllo utente). Il codice sorgente per questo controllo è quasi identico a quello dell'esempio autoclaims con due differenze:

-   La `AutoClaims` classe in questo esempio eredita dalla classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) anziché dalla classe del [form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) .

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   La classe autoclaims in questo esempio dispone di un metodo pubblico aggiunto, `DisposeResources` che elimina i controlli figlio interni utilizzati per la raccolta di input penna. Questo metodo deve essere chiamato da thewebpageon, che viene utilizzato dal controllo al termine dell'utilizzo del controllo da parte della pagina.

## <a name="referencing-the-control-in-html"></a>Riferimento al controllo in HTML

La soluzione include un file HTML, default.htm. Questo file è la pagina a cui viene spostato il browser per caricare il controllo. Il file contiene un <object> tag che fa riferimento al controllo. Include anche uno script che viene chiamato quando la pagina viene scaricata, come indicato dalla presenza dell'attributo onload = " `OnUnload()` " nel <body> Tag. Questa funzione chiama il `DisposeResources` metodo sul controllo per assicurarsi che tutte le risorse vengano rilasciate correttamente al momento dell'arresto.


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



Si noti il formato del valore dell'attributo ClassID per il <object> tag. Assegna un nome all'assembly, seguito da un \# separatore di segno, quindi dallo spazio dei nomi che contiene il controllo e quindi dal nome della classe del controllo.

Un controllo utente reale può probabilmente includere metodi aggiuntivi usati per salvare in modo permanente o inviare i dati raccolti nell'applicazione.

## <a name="the-autoclaims_webcontrol-project"></a>Il progetto WebControl autoclaims \_

Il progetto WebControl autoclaims \_ è un progetto di distribuzione che crea un'installazione che aggiunge una radice virtuale, ovvero Autoclaims \_ WebControl, nel server Web al momento dell'installazione. Il controllo e il file HTML vengono inseriti in questa radice virtuale.

> [!Note]  
> Gli esempi Web compilati non vengono installati tramite l'opzione di installazione predefinita per l'SDK. È necessario completare un'installazione personalizzata e selezionare l'opzione secondaria "esempi Web precompilati" per installarli.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di modulo Claims automatico](auto-claims-form-sample.md)
</dt> <dt>

[Input penna sul Web](ink-on-the-web.md)
</dt> </dl>

 

 
