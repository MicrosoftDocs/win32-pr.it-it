---
title: Sintassi del gruppo di effetti (Direct3D 11)
description: Un gruppo di effetti viene dichiarato con la sintassi descritta in questa sezione.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9221341810990801f1ed07005e0dcb917df42360
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104472046"
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
| <span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup<br/>                                                                                                         | parola chiave ecessario.<br/>                                                                                                                                                                                                         |
| <span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName<br/>                                                                       | Obbligatorio. Stringa ASCII che identifica in modo univoco il nome del gruppo di effetti. Diversamente dalle tecniche, i gruppi devono avere nomi per assicurarsi che le tecniche abbiano un identificatore univoco (vedere la sezione relativa a gruppi e tecniche di seguito).<br/> |
| <span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> Annotazioni < ><br/> | \[in \] facoltativo. Una o più parti di informazioni (metadati) fornite dall'utente ignorate dal sistema di effetti. Per la sintassi, vedere Sintassi delle annotazioni (Direct3D 11). <br/>                                                      |
| <span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/>                                           | "Technique10" o "technique11". Le tecniche che usano la nuova funzionalità di Direct3D 11 (5 \_ 0 Shader, BindInterfaces e così via) devono usare "technique11".<br/>                                                                 |
| <span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>Techniquename<br/>                                                       | facoltativo. Stringa ASCII che identifica in modo univoco il nome della tecnica degli effetti. <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a>Gruppi e tecniche

Per mantenere la compatibilità con \_ \_ gli effetti FX 4 0, i gruppi sono facoltativi. È presente un gruppo implicito con nome NULL che circonda tutte le tecniche globali.

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



In C++, è possibile ottenere una tecnica in base al nome in due modi. I comandi seguenti troveranno le tecniche più ovvie:


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



Per assicurarsi che [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) funzioni in modo analogo agli effetti 10, tutti i gruppi definiti devono avere un nome.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](d3d11-effect-format.md)
</dt> <dt>

[Sintassi della tecnica degli effetti (Direct3D 11)](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





