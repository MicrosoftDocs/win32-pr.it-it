---
description: Vedere un elenco di flag di funzionalità del driver D3DCAPS2. Include definizioni, valori e descrizioni con collegamenti alle API.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fc58f0e249a90a325631123ce7b8e43d4149a7244e7b2032c489c0999137ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989121"
---
# <a name="d3dcaps2"></a>D3DCAPS2

Flag di funzionalità del driver.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definire</td>
<td>Valore</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANAUTOGENMIPMAP</td>
<td>0x40000000L</td>
<td>Il driver è in grado di generare automaticamente mipmap. Per altre informazioni, vedere <a href="automatic-generation-of-mipmaps.md">Generazione automatica di mipmap (Direct3D 9).</a></td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANCALIBRATEGAMMA</td>
<td>0x00100000L</td>
<td>Nel sistema è installato un calibratore in grado di regolare automaticamente la rampa gamma in modo che il risultato sia identico in tutti i sistemi con calibrazione. Per richiamare il calibratore quando si impostano nuovi livelli gamma, usare il flag D3DSGR_CALIBRATE quando si <a href="/windows/desktop/api"><strong>chiama SetGammaRamp</strong></a>. La calibrazione delle rampe gamma comporta un sovraccarico di elaborazione e non deve essere usata di frequente.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANSHARERESOURCE</td>
<td>0x80000000L</td>
<td>Il dispositivo può creare risorse condivise. I metodi che creano risorse possono impostare valori non NULL per i <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>parametri pSharedHandle.</strong></a> 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANMANAGERESOURCE</td>
<td>0x10000000L</td>
<td>Il driver è in grado di gestire le risorse. In questi driver, D3DPOOL_MANAGED risorse verranno gestite dal driver. Per fare in modo che Direct3D ese sostituisca il driver in modo che Direct3D gestirà le risorse, usare il flag D3DCREATE_DISABLE_DRIVER_MANAGEMENT quando si chiama <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_DYNAMICTEXTURES</td>
<td>0x20000000L</td>
<td>Il driver supporta trame dinamiche.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_FULLSCREENGAMMA</td>
<td>0x00020000L</td>
<td>Il driver supporta la regolazione dinamica della rampa gamma in modalità schermo intero.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_RESERVED</td>
<td>0x02000000L</td>
<td>Riservato; non usato.</td>
</tr>
</tbody>
</table>



 

Queste costanti vengono usate dal membro D3CAPS2 di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informazioni costanti



|  Requisito                        | Valore           |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
