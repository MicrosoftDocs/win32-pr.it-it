---
description: Se si utilizza l'API di scripting per WMI, è possibile impostare privilegi di sicurezza specifici.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Esecuzione di operazioni con privilegi tramite VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131975"
---
# <a name="executing-privileged-operations-using-vbscript"></a>Esecuzione di operazioni con privilegi tramite VBScript

Se si utilizza l'API di scripting per WMI, è possibile impostare privilegi di sicurezza specifici. Ad esempio, è possibile impostare i privilegi di sicurezza per richiedere l'arresto di un sistema operativo o per esaminare il registro eventi di protezione. Per ulteriori informazioni, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).

È necessario impostare i privilegi solo quando si accede a WMI nel computer. Quando si accede a un host remoto, in COM RPC i privilegi vengono impostati automaticamente. Per determinare tutti i privilegi richiesti, consultare la documentazione per le classi WMI specifiche a cui si vuole accedere, ad esempio [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem). Per ulteriori informazioni, vedere [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)

Le sezioni seguenti sono illustrate in questo argomento:

-   [Impostazione di un privilegio dall'oggetto di sicurezza \_](/windows)
-   [Impostazione di un privilegio come parte di un moniker](#setting-a-privilege-as-part-of-a-moniker)
-   [Revoca e reimpostazione dei privilegi](#revoking-and-resetting-privileges)
-   [Argomenti correlati](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a>Impostazione di un privilegio dall'oggetto di sicurezza \_

Utilizzare la procedura seguente per impostare i privilegi di sicurezza in Visual Basic.

**Per impostare i privilegi in Visual Basic**

1.  Creare un oggetto di tipo [**SWbemLocator**](swbemlocator.md).
2.  Aggiungere il nuovo privilegio all'oggetto [**SWbemLocator. Security \_**](swbemlocator-security-.md) .

    L'oggetto di [**sicurezza \_**](swbemlocator-security-.md) contiene una raccolta [**SWbemObjectSet**](swbemobjectset.md) . Gli oggetti nel set sono oggetti [**SWbemSecurity**](swbemsecurity.md) . Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).

3.  Accedere a WMI e recuperare un oggetto [**SWbemServices**](swbemservices.md) .

    L'oggetto [**SWbemServices**](swbemservices.md) eredita il privilegio impostato nel passaggio precedente.

È anche possibile impostare un privilegio usando il metodo [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) .

## <a name="setting-a-privilege-as-part-of-a-moniker"></a>Impostazione di un privilegio come parte di un moniker

È possibile impostare un privilegio come parte di un moniker.

Nell'esempio seguente viene illustrato come aggiungere un privilegio di debug a un moniker.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a>Revoca e reimpostazione dei privilegi

Nell'esempio seguente viene illustrato come impostare il privilegio **SeDebugPrivilege** e revocare il privilegio **SeRemoteShutdownPrivilege** .


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti Privilege**](privilege-constants.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi](executing-privileged-operations.md)
</dt> </dl>

 

 
