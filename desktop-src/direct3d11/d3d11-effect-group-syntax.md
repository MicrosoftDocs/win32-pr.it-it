---
title: Sintassi del gruppo di effetti (Direct3D 11)
description: Un gruppo di effetti viene dichiarato con la sintassi descritta in questa sezione.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c1b2c72b0a67a31911a0f2c9f9ae6ac0e9e20463a850c303dab4a208401d1c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069751"
---
# <a name="effect-group-syntax-direct3d-11"></a>Sintassi del gruppo di effetti (Direct3D 11)

Un gruppo di effetti viene dichiarato con la sintassi descritta in questa sezione.


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a>Parametri



| Elemento                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup<br/>                                                                                                         | Parola chiave equired.<br/>                                                                                                                                                                                                         |
| <span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>Groupname<br/>                                                                       | Obbligatorio. Stringa ASCII che identifica in modo univoco il nome del gruppo di effetti. A differenza delle tecniche, i gruppi devono avere nomi per garantire che le tecniche hanno un identificatore univoco (vedere la sezione Gruppi e tecniche più avanti).<br/> |
| <span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < annotazioni ><br/> | \[in \] Facoltativo. Una o più informazioni fornite dall'utente (metadati) che vengono ignorate dal sistema di effetti. Per la sintassi, vedere Sintassi delle annotazioni (Direct3D 11). <br/>                                                      |
| <span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/>                                           | "technique10" o "technique11". Le tecniche che usano funzionalità nuove di Direct3D 11 (5 \_ shader 0, BindInterfaces e così via) devono usare "technique11".<br/>                                                                 |
| <span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName<br/>                                                       | facoltativo. Stringa ASCII che identifica in modo univoco il nome della tecnica dell'effetto. <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a>Gruppi e tecniche

Per mantenere la compatibilità con gli effetti fx \_ 4 \_ 0, i gruppi sono facoltativi. Esiste un gruppo implicito denominato NULL che circonda tutte le tecniche globali.

Si consideri l'esempio seguente:


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



In C++ è possibile ottenere una tecnica in base al nome in due modi. I comandi seguenti troveranno le tecniche ovvie:


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



Per garantire che [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) funzioni in modo analogo a Effects 10, tutti i gruppi definiti devono avere un nome.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](d3d11-effect-format.md)
</dt> <dt>

[Sintassi della tecnica degli effetti (Direct3D 11)](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





