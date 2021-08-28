---
description: Questo esempio illustra come creare un controllo abilitato per l'input penna da usare in un Web browser. L'esempio accetta l'esempio di modulo delle attestazioni automatico originale e lo trasforma in un controllo inserito in una pagina Web.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Esempio di controllo Web Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe2035028ab622f896489b304ca850db4e25462
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882047"
---
# <a name="ink-web-control-sample"></a>Esempio di controllo Web Ink

Questo esempio illustra come creare un controllo abilitato per l'input penna da usare in un Web browser. L'esempio accetta [l'esempio di modulo](auto-claims-form-sample.md) delle attestazioni automatico originale e lo trasforma in un controllo inserito in una pagina Web.

Per altre informazioni sull'uso dell'input penna sul Web, vedere [Input penna sul Web](ink-on-the-web.md).

## <a name="modifications-to-the-original-sample-project"></a>Modifiche al modello di esempio Project

Questo esempio è costituito da una soluzione che include due progetti e un file HTML. Il primo progetto, AutoClaims, è un progetto libreria di controlli Di Microsoft Visual C \# (un controllo utente). Il codice sorgente per questo controllo è quasi identico a quello dell'esempio AutoClaims con due differenze:

-   La `AutoClaims` classe in questo esempio eredita dalla classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) anziché dalla [classe Form.](/dotnet/api/system.windows.forms.form?view=netcore-3.1)

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   La classe AutoClaims in questo esempio include un metodo pubblico aggiunto, che elimina i controlli figlio interni usati per la raccolta `DisposeResources` dell'input penna. Questo metodo deve essere chiamato dalla pagina Web su cui viene usato il controllo quando la pagina termina di usare il controllo .

## <a name="referencing-the-control-in-html"></a>Riferimento al controllo in HTML

La soluzione include un file HTML, default.htm. Questo file è la pagina a cui il browser passa per caricare il controllo. Il file contiene un &lt; tag oggetto che fa riferimento al controllo &gt; . Include anche uno script che viene chiamato quando la pagina viene scaricata, come indicato dalla presenza dell'attributo onload=" `OnUnload()` " nel tag del &lt; &gt; corpo. Questa funzione chiama il metodo sul controllo per assicurarsi che tutte le risorse `DisposeResources` siano rilasciate correttamente all'arresto.


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



Si noti il formato del valore dell'attributo classid per il &lt; tag &gt; dell'oggetto. Denota l'assembly, seguito da un separatore di segno, quindi lo spazio dei nomi che contiene il controllo e quindi il nome \# della classe del controllo.

Un controllo utente reale include probabilmente metodi aggiuntivi usati per rendere persistenti o inviare i dati raccolti nell'applicazione.

## <a name="the-autoclaims_webcontrol-project"></a>Controllo Web AutoClaims \_ Project

Il progetto AutoClaims WebControl è un Project di distribuzione che crea un'installazione che aggiunge una radice \_ virtuale, AutoClaims WebControl, nel server Web al momento \_ dell'installazione. Il controllo e il file HTML vengono inseriti in questa radice virtuale.

> [!Note]  
> Gli esempi Web compilati non vengono installati dall'opzione di installazione predefinita per l'SDK. È necessario completare un'installazione personalizzata e selezionare l'opzione secondaria "Esempi Web precompilato" per installarli.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di modulo attestazioni automatico](auto-claims-form-sample.md)
</dt> <dt>

[Input penna sul Web](ink-on-the-web.md)
</dt> </dl>

 

 
