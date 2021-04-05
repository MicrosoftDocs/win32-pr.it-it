---
title: Condivisione surrogati
description: I server DLL condivideranno un surrogato se hanno identità di sicurezza corrispondenti e condividono lo stesso valore AppID.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709424"
---
# <a name="surrogate-sharing"></a>Condivisione surrogati

I server DLL condivideranno un surrogato se hanno identità di sicurezza corrispondenti e condividono lo stesso valore AppID.

Per impostazione predefinita, i server DLL vengono caricati nel proprio processo surrogato. Per caricare altri server DLL in un surrogato esistente in modo che supporti più di un server DLL, esistono due requisiti:

-   I server DLL devono avere lo stesso valore AppID.
-   Il contesto di sicurezza dei server DLL deve essere lo stesso.

Se due server DLL devono essere avviati con diverse identità di sicurezza, devono trovarsi in surrogati diversi, indipendentemente dal fatto che i rispettivi AppID corrispondano.

Di seguito è riportato un esempio di amministrazione della condivisione surrogata con AppID:

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

I due CLSID per i componenti DLL comp1.dll e comp2.dll sono stati configurati per la condivisione di un AppID. La chiave [AppID](appid-key.md) specifica che il server dll può essere caricato in un surrogato specificando il valore [DllSurrogate](dllsurrogate.md) . In questo esempio, il valore **DllSurrogate** è una stringa vuota, che indica che deve essere utilizzata l'implementazione di sistema predefinita del surrogato della dll.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Requisiti del server DLL](dll-server-requirements.md)
</dt> <dt>

[Registrazione del server DLL per l'attivazione surrogata](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




