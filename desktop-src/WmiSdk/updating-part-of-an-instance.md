---
description: Occasionalmente, potrebbe essere necessario aggiornare solo parte di un'istanza.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Aggiornamento di una parte di un'istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309757"
---
# <a name="updating-part-of-an-instance"></a>Aggiornamento di una parte di un'istanza

Occasionalmente, potrebbe essere necessario aggiornare solo parte di un'istanza. Ad esempio, alcune istanze hanno un numero elevato di proprietà. Se è necessario aggiornare un numero elevato di istanze, è possibile ridurre le prestazioni del sistema. Pertanto, è possibile scegliere di aggiornare solo una parte dell'istanza di e quindi ridurre la quantità di informazioni che è necessario inviare e recuperare da e in WMI. Tuttavia, WMI non supporta direttamente le operazioni di istanza parziale, né la maggior parte dei provider. Pertanto, se si scrive un'applicazione che usa operazioni a istanza parziale, prepararsi per le chiamate a non riuscire con **il \_ provider WBEM e \_ \_ non \_ in grado** di supportare il codice di errore **WBEM \_ e \_ non \_ supportato** in C++. Nei linguaggi di scripting i codici di errore sono **wbemErrProviderNotCapable** o **wbemErrNotSupported**.

Nello scripting questa operazione è necessaria solo per aiutare le prestazioni quando si aggiornano una o due proprietà scrivibili in un numero molto elevato di oggetti in un'organizzazione. In caso contrario, le normali chiamate VBScript a [**SWbemObject \_ . Put**](swbemobject-put-.md) o [**SWbemObject \_ . PutAsync**](swbemobject-putasync-.md), mentre sembrano scrivere l'intero oggetto, aggiornano in realtà solo le proprietà che il provider ha abilitato per la scrittura.

Nella procedura seguente viene descritto come richiedere un aggiornamento parziale dell'istanza tramite PowerShell.

**Per richiedere un aggiornamento parziale dell'istanza tramite PowerShell**

1.  Recuperare il percorso dell'oggetto che si desidera aggiornare.

    È possibile descrivere il percorso manualmente, altrimenti eseguire una query sull'oggetto e recuperare la proprietà **\_ \_ path** .

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  Configurare una tabella hash che elenca i nomi delle proprietà da aggiornare e usare questa tabella hash in una chiamata a [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

Nella procedura seguente viene descritto come richiedere un aggiornamento parziale dell'istanza tramite C#.

> [!Note]  
> **System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.

 

**Per richiedere un aggiornamento parziale dell'istanza tramite C #**

1.  Creare un nuovo oggetto [ManagementObject](/dotnet/api/system.management.managementobject) che rappresenta l'istanza specifica da aggiornare.

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  Impostare il valore della proprietà con una chiamata a [ManagementObject. sepropertyvalue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

Nella procedura seguente viene descritto come richiedere un aggiornamento parziale dell'istanza tramite VBScript.

**Per richiedere un aggiornamento parziale dell'istanza tramite VBScript**

1.  Creare un oggetto contesto [**SWbemNamedValueSet**](swbemnamedvalueset.md) .

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  Aggiungere i valori di estensione PUT " \_ \_ put \_ Extensions" e " \_ \_ put \_ ext \_ client \_ Request" all'oggetto context usando il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  Configurare una matrice in cui sono elencati i nomi delle proprietà da aggiornare e aggiungere questa matrice all'oggetto contesto [**SWbemNamedValueSet**](swbemnamedvalueset.md) con il valore di estensione PUT " \_ \_ put \_ ext \_ Properties".

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  Impostare il parametro *iFlags* della chiamata [**SWbemObject. put \_**](swbemobject-put-.md) su **wbemChangeFlagUpdateOnly**. Senza questo flag la chiamata avrà esito negativo con un contesto non valido.

5.  Passare il flag e l'oggetto di contesto al provider nel parametro *objwbemNamedValueSet* di [**SWbemObject. put \_**](swbemobject-put-.md) o [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md).

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

Nella procedura riportata di seguito viene descritto come richiedere un aggiornamento parziale dell'istanza mediante C++.

**Per richiedere un aggiornamento parziale dell'istanza con C++**

1.  Creare un oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Un oggetto context è un oggetto utilizzato da WMI per passare ulteriori informazioni a un provider WMI. In questo caso, si usa l'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) per indicare al provider di accettare gli aggiornamenti parziali dell'istanza.

2.  Aggiungere i \_ \_ \_ valori denominati "put Extensions" e " \_ \_ put \_ ext \_ client \_ Request" all'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una chiamata a [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).

    La tabella seguente elenca il significato di " \_ \_ put \_ Extensions" e " \_ \_ put \_ ext \_ client \_ Request".

    

    | Valore denominato                     | Descrizione                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | " \_ \_ Inserisci \_ estensioni"           | **VT \_ BOOL** impostato su **Variant \_ true**. Valore che indica che sono stati specificati uno o più valori di contesto. Questo consente un rapido controllo dell'oggetto contesto all'interno del provider per determinare se vengono utilizzati gli aggiornamenti parziali dell'istanza. |
    | " \_ \_ Inserisci \_ \_ richiesta client ext \_ " | **VT \_ BOOL** impostato su **Variant \_ true**. Impostato dal client durante la richiesta iniziale. Questo valore viene utilizzato per evitare errori di rientranza.                                                                                                                   |

    

     

3.  Aggiungere le \_ \_ \_ proprietà put ext \_ strict \_ null, \_ \_ put \_ ext \_ Properties o \_ \_ put \_ ext \_ Atomic in qualsiasi combinazione, in base alle esigenze, all'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con un'altra chiamata a [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).

    Nella tabella seguente viene elencato il significato dei valori denominati.

    

    | Valore denominato                   | Descrizione                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | " \_ \_ put \_ ext \_ strict \_ nulls" | **VT \_ BOOL** impostato su **Variant \_ true**. Indica che il client ha intenzionalmente impostato le proprietà su **VT \_ null** e prevede che l'operazione di scrittura abbia esito positivo. Se il provider non è in grado di impostare i valori su **null**, è necessario segnalare un errore. |
    | " \_ \_ put \_ ext \_ Properties"    | [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) di stringhe contenente un elenco di nomi di proprietà da aggiornare. Può essere usato da solo o in combinazione con " \_ \_ put \_ ext \_ Properties". I valori si trovano nell'istanza di in fase di scrittura.                           |
    | " \_ \_ put \_ ext \_ Atomic"        | **VT \_ BOOL** impostato su **Variant \_ true**. Indica che tutti gli aggiornamenti devono avere esito positivo simultaneo (semantica atomica) o che il provider deve essere ripristinato. Non è possibile avere esito positivo parziale. Può essere usato da solo o in combinazione con altri flag.     |

    

     

4.  Impostare il parametro *iFlags* solo per l' **\_ \_ aggiornamento \_ del flag WBEM**. Senza questo flag la chiamata avrà esito negativo con un contesto non valido.
5.  Passare l'oggetto contesto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) in qualsiasi chiamata [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) nel parametro *pctX* .

    Il passaggio dell'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) indica al provider di consentire aggiornamenti parziali dell'istanza. In un aggiornamento dell'istanza completa, è necessario impostare *pctX* su **null**.

    Il provider può scrivere eventuali proprietà necessarie se l'oggetto contesto presente nella chiamata non contiene " \_ \_ put \_ Extensions". Se \_ \_ \_ nell'oggetto context è presente "put Extensions", per WMI è necessario che il provider rispetti la semantica dell'operazione in modo esatto. in caso contrario, la chiamata non riesce. Per ulteriori informazioni, vedere [gestione dei messaggi di accesso negato in un provider](impersonating-a-client.md).

 

 
