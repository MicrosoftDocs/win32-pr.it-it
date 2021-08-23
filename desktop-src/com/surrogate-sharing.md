---
title: Condivisione di surrogati
description: I server DLL condivideranno un surrogato se hanno identità di sicurezza corrispondenti e condividono lo stesso valore AppID.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e159fff59144773633cfbe35bb1486e9eeb1014d02e23e0c9b95bcd817bb53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678411"
---
# <a name="surrogate-sharing"></a>Condivisione di surrogati

I server DLL condivideranno un surrogato se hanno identità di sicurezza corrispondenti e condividono lo stesso valore AppID.

I server DLL vengono caricati, per impostazione predefinita, nel proprio processo surrogato. Per caricare altri server DLL in un surrogato esistente in modo che supporti più di un server DLL, sono necessari due requisiti:

-   I server DLL devono avere lo stesso valore AppID.
-   Il contesto di sicurezza dei server DLL deve essere lo stesso.

Se due server DLL devono essere avviati con identità di sicurezza diverse, devono essere in surrogati diversi, indipendentemente dal fatto che i relativi AppID corrispondano.

Di seguito è riportato un esempio di amministrazione della condivisione di surrogati con Gli AppID:

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

I due CLSID per i componenti DLL comp1.dll e comp2.dll sono stati configurati per condividere un AppID. La [chiave AppID](appid-key.md) specifica che il server DLL può essere caricato in un surrogato specificando il [valore DllSurrogate.](dllsurrogate.md) In questo esempio il **valore DllSurrogate** è una stringa vuota, a indicare che deve essere usata l'implementazione di sistema predefinita del surrogato dll.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Requisiti del server DLL](dll-server-requirements.md)
</dt> <dt>

[Registrazione del server DLL per l'attivazione surrogata](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




