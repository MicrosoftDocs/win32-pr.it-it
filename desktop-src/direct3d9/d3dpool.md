---
description: Definisce la classe di memoria che include i buffer per una risorsa.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: Enumerazione D3DPOOL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322924"
---
# <a name="d3dpool-enumeration"></a>Enumerazione D3DPOOL

Definisce la classe di memoria che include i buffer per una risorsa.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**\_Impostazione predefinita D3DPOOL**
</dt> <dd>

Le risorse vengono inserite nel pool di memoria più appropriato per il set di utilizzi richiesti per la risorsa specificata. Si tratta in genere di memoria video, inclusa la memoria video locale e la memoria AGP. Il \_ pool predefinito D3DPOOL è separato da D3DPOOL \_ Managed e D3DPOOL \_ SYSTEMMEM e specifica che la risorsa viene posizionata nella memoria preferita per l'accesso al dispositivo. Si noti che D3DPOOL \_ default non indica mai che D3DPOOL \_ Managed o D3DPOOL \_ SYSTEMMEM deve essere scelto come tipo di pool di memoria per questa risorsa. Le trame posizionate nel \_ pool predefinito D3DPOOL non possono essere bloccate a meno che non siano trame dinamiche oppure sono formati di driver privati, FourCC e. Per accedere a trame sbloccabili, è necessario usare funzioni quali [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9:: GetFrontBufferData**](/windows/desktop/api)e [**IDirect3DDevice9:: GetRenderTargetData**](/windows/desktop/api). D3DPOOL \_ Managed è probabilmente una scelta migliore rispetto \_ a D3DPOOL default per la maggior parte delle applicazioni. Si noti che alcune trame create in formati pixel proprietari del driver, sconosciute al runtime Direct3D, possono essere bloccate. Si noti anche che, a differenza delle trame, è possibile bloccare i buffer indietro della catena di scambio, le destinazioni di rendering, i buffer dei vertici e i buffer di indice. Quando un dispositivo viene perso, è necessario rilasciare le risorse create con D3DPOOL \_ default prima di chiamare [**IDirect3DDevice9:: Reset**](/windows/desktop/api). Per altre informazioni, vedere [dispositivi persi (Direct3D 9)](lost-devices.md).

Quando si creano risorse con D3DPOOL \_ predefinito, se è già stato eseguito il commit della memoria della scheda video, le risorse gestite verranno rimosse per liberare memoria sufficiente per soddisfare la richiesta.

</dd> <dt>

<span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL \_ gestito**
</dt> <dd>

Le risorse vengono copiate automaticamente nella memoria accessibile dal dispositivo in base alle esigenze. Le risorse gestite sono supportate dalla memoria di sistema e non devono essere ricreate quando un dispositivo viene perso. Per ulteriori informazioni, vedere [gestione delle risorse (Direct3D 9)](managing-resources.md) . È possibile bloccare le risorse gestite. Viene direttamente modificata solo la copia della memoria di sistema. Direct3D copia le modifiche apportate alla memoria accessibile dal driver in base alle esigenze.



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> D3DPOOL \_ gestito è valido con [**IDirect3DDevice9**](/windows/desktop/api); tuttavia, non è valido con [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).<br/> |



 

</dd> <dt>

<span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**\_SYSTEMMEM D3DPOOL**
</dt> <dd>

Le risorse vengono inserite in memoria che in genere non è accessibile dal dispositivo Direct3D. Questa allocazione di memoria utilizza la RAM di sistema, ma non riduce la RAM paginabile. Queste risorse non devono essere ricreate quando un dispositivo viene perso. Le risorse in questo pool possono essere bloccate e possono essere usate come origine per un'operazione [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api) o [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) in una risorsa di memoria creata con D3DPOOL \_ valore predefinito.

</dd> <dt>

<span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_ Scratch**
</dt> <dd>

Le risorse vengono inserite nella RAM di sistema e non devono essere ricreate quando un dispositivo viene perso. Queste risorse non sono vincolate dalle dimensioni del dispositivo o dalle restrizioni di formato. Per questo motivo, non è possibile accedere a queste risorse dal dispositivo Direct3D né impostare come destinazioni di rendering o trame. Tuttavia, queste risorse possono sempre essere create, bloccate e copiate.

</dd> <dt>

<span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutti i tipi di pool sono validi con tutte le risorse, tra cui: buffer dei vertici, buffer di indice, trame e superfici.

Le tabelle seguenti indicano restrizioni sui tipi di pool per le destinazioni di rendering, gli stencil di profondità e gli utilizzi dinamici e mipmap. Una x indica una combinazione compatibile. la mancanza di una x indica l'incompatibilità.



| Pool               | \_RENDERTARGET D3DUSAGE | \_DEPTHSTENCIL D3DUSAGE |
|--------------------|------------------------|------------------------|
| \_Impostazione predefinita D3DPOOL   | x                      | x                      |
| D3DPOOL \_ gestito   |                        |                        |
| D3DPOOL \_ Scratch   |                        |                        |
| \_SYSTEMMEM D3DPOOL |                        |                        |



 



| Pool               | D3DUSAGE \_ dinamico | \_AUTOGENMIPMAP D3DUSAGE |
|--------------------|-------------------|-------------------------|
| \_Impostazione predefinita D3DPOOL   | x                 | x                       |
| D3DPOOL \_ gestito   |                   | x                       |
| D3DPOOL \_ Scratch   |                   |                         |
| \_SYSTEMMEM D3DPOOL | x                 |                         |



 

Per ulteriori informazioni sui tipi di utilizzo, vedere [**D3DUSAGE**](d3dusage.md).

Non è possibile combinare i pool per oggetti diversi contenuti all'interno di una risorsa (livelli MIP in una mipmap) e, quando si sceglie un pool, non è possibile modificarli.

Le applicazioni devono usare D3DPOOL \_ gestiti per la maggior parte delle risorse statiche, perché questo evita che l'applicazione debba gestire i dispositivi smarriti. (Le risorse gestite vengono ripristinate dal Runtime). Questa operazione è particolarmente utile per i sistemi di architettura della memoria unificata (UMA). Altre risorse dinamiche non sono una corrispondenza corretta per D3DPOOL \_ gestito. In realtà, i buffer di indice e i buffer dei vertici non possono essere creati usando D3DPOOL \_ gestiti insieme a D3DUSAGE \_ Dynamic.

Per le trame dinamiche è talvolta consigliabile usare una coppia di trame di memoria video e di memoria di sistema, allocando la memoria video usando D3DPOOL \_ default e la memoria di sistema usando D3DPOOL \_ SYSTEMMEM. È possibile bloccare e modificare i bit della trama della memoria di sistema usando un metodo di blocco. È quindi possibile aggiornare la trama della memoria video usando [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DUSAGE**](d3dusage.md)
</dt> <dt>

[**IDirect3DDevice9:: CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[**IDirect3DDevice9:: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[**IDirect3DDevice9:: CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[**D3DINDEXBUFFER \_ DESC**](d3dindexbuffer-desc.md)
</dt> <dt>

[**D3DSURFACE \_ DESC**](d3dsurface-desc.md)
</dt> <dt>

[**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md)
</dt> <dt>

[**D3DVOLUME \_ DESC**](d3dvolume-desc.md)
</dt> </dl>

 

 
