---
title: Programmazione di ADSI con Java/COM
description: Utilizzando Microsoft Virtual Machine per Java (Microsoft VM) e il compilatore Java Microsoft, è possibile accedere a tutte le funzionalità ADSI esposte tramite i componenti COM ADSI, da un'applicazione Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programmazione di ADSI con AD Java/COM
- ADSI ADSI, uso, programmazione Java/COM per
- ADSI ADSI, codice di esempio Java
- ADSI ADSI, esempio di codice Java, associazione a un oggetto ADSI e richiamo di metodi su tale oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855266"
---
# <a name="programming-adsi-with-javacom"></a>Programmazione di ADSI con Java/COM

Utilizzando Microsoft Virtual Machine per Java (Microsoft VM) e il compilatore Java Microsoft, è possibile accedere a tutte le funzionalità ADSI esposte tramite i componenti COM ADSI, da un'applicazione Java/COM. Nell'esempio di codice Java riportato di seguito vengono illustrati gli elementi necessari per eseguire l'associazione a un oggetto ADSI e richiamare metodi su tale oggetto. Le funzioni e i metodi degli oggetti dell'API ADSI richiesti vengono esposti tramite Activeds.dll.


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



L'argomento nella prima istruzione **Import** fa riferimento alle classi wrapper Java incluse in Activeds.dll. Utilizzare Visual J++ per creare le classi wrapper e includerle nel progetto, attenendosi alla procedura riportata di seguito.

**Per creare classi wrapper e includerle nel progetto**

1.  In un progetto Visual J++ selezionare **Aggiungi wrapper com...** dal menu **progetto** .
2.  Selezionare "Active DS Type Library" dalla finestra di dialogo **componenti installati:** dalla finestra di dialogo wrapper com. Se la libreria dei tipi non è visualizzata nella casella di riepilogo, fare clic sul pulsante **Sfoglia** , passare alla directory in cui è archiviato activeds. tlb, quindi selezionare la libreria dei tipi.

Visual J++ crea il pacchetto activeds per le classi wrapper Java e include il pacchetto nel percorso predefinito del progetto. Per ulteriori informazioni, vedere il pacchetto activeds nel riquadro **Esplora progetti** della finestra Visual J++.

Per ottenere un oggetto ADSI che non può essere cocreato, usare una delle funzioni dell'API ADSI esposte, ad esempio, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), che vengono anche assemblate in Activeds.dll. Microsoft J/Direct fornisce l'accesso a queste e ad altre API native. Questa operazione è illustrata nelle ultime due righe dell'esempio di codice, sopra.

Quando si esegue la compilazione, assicurarsi che l'estensione del linguaggio Microsoft sia abilitata. A tale scopo, selezionare **<project> Proprietà** dal menu **progetto** nella finestra del progetto Visual J++. Quindi, fare clic sulla scheda **Compila** nella finestra di dialogo **<project> proprietà** . Deselezionare la casella di controllo **Disabilita estensioni Microsoft Language** . Se si esegue la compilazione dalla riga di comando, usare l'opzione "/x-", ad esempio:

**JVC/x-SimpleADSI. Java**

Infine, per consentire alla macchina virtuale di caricare il componente COM, la libreria di collegamento dinamico (DLL) deve essere visibile sul percorso di sistema. Se viene restituito un errore "Java. lang. UnsatisfiedLinkError", impostare il percorso in modo da includere il percorso che contiene la DLL richiesta. Se ad esempio Activeds.dll è stato installato in c: \\ ADSI \\ lib, eseguire il comando seguente dalla riga di comando:

**Imposta percorso =% PATH%; c: \\ ADSI \\ lib**

 

 




