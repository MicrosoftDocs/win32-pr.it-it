---
title: Programmazione di ADSI con Java/COM
description: Usando la macchina virtuale Microsoft per Java (Microsoft VM) e il compilatore Microsoft Java, è possibile accedere a tutte le funzionalità ADSI esposte tramite tutti i componenti COM ADSI, da un'applicazione Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programmazione di ADSI con Java/COM AD
- ADSI ADSI , uso, programmazione Java/COM per
- ADSI ADSI , codice di esempio Java
- ADSI ADSI , codice java di esempio, associazione a un oggetto ADSI e chiamata di metodi su tale oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec873822d27a7b5fcf95aad7c31a8978552eb88
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880294"
---
# <a name="programming-adsi-with-javacom"></a>Programmazione di ADSI con Java/COM

Usando la macchina virtuale Microsoft per Java (Microsoft VM) e il compilatore Microsoft Java, è possibile accedere a tutte le funzionalità ADSI esposte tramite tutti i componenti COM ADSI, da un'applicazione Java/COM. Nell'esempio di codice Java seguente vengono illustrati gli elementi necessari per eseguire l'associazione a un oggetto ADSI e richiamare i metodi su tale oggetto. Le funzioni API ADSI necessarie e i metodi dell'oggetto vengono esposti tramite Activeds.dll.


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



L'argomento nella prima **istruzione import** fa riferimento alle classi Wrapper Java in pacchetto in Activeds.dll. Usare Visual J++ per creare le classi wrapper e includerle nel progetto, seguendo la procedura seguente.

**Per creare classi wrapper e includerle nel progetto**

1.  In un progetto Visual J++ selezionare **Aggiungi wrapper Com...** dal menu **Project** codice.
2.  Selezionare "Active DS Type Library" nella **finestra di dialogo Componenti installati:** nella finestra di dialogo Wrapper COM. Se la libreria dei tipi non viene  visualizzata nella casella di riepilogo, fare clic sul pulsante Sfoglia, passare alla directory in cui è archiviato Activeds.tlb e quindi selezionare la libreria dei tipi.

Visual J++ crea il pacchetto activeds per le classi Wrapper Java e include il pacchetto nel percorso predefinito del progetto. Per altre informazioni, vedere il pacchetto activeds **nel riquadro Esplora Project** nella finestra di Visual J++.

Per ottenere un oggetto ADSI che non può essere cocreato, usare una delle funzioni API ADSI esposte, ad esempio [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), che sono anche in pacchetto in Activeds.dll. Microsoft J/Direct fornisce l'accesso a queste e ad altre API native. Questo è illustrato dalle ultime due righe dell'esempio di codice precedente.

Durante la compilazione, assicurarsi che l'estensione del linguaggio Microsoft sia abilitata. A tale scopo, selezionare **&lt; Proprietà &gt; progetto...** dal **menu** Project nella finestra del progetto Visual J++. Fare quindi clic sulla **scheda Compila** nella finestra di **&lt; dialogo &gt; Proprietà** progetto. Deselezionare **la casella di controllo Disabilita estensioni del linguaggio Microsoft** . Se si esegue la compilazione dalla riga di comando, usare l'opzione "/x-", ad esempio:

**jvc /x- SimpleADSI.java**

Infine, per consentire alla macchina virtuale di caricare il componente COM, la libreria a collegamento dinamico (DLL) deve essere visibile nel percorso di sistema. Se viene restituito un errore "java.lang.UnsatisfiedLinkError", impostare PATH in modo da includere il percorso che contiene la DLL richiesta. Ad esempio, se Activeds.dll è stato installato in \\ c:adsi \\ lib, eseguire il comando seguente dalla riga di comando:

**set PATH = %PATH%; c: \\ adsi \\ lib**

 

 




