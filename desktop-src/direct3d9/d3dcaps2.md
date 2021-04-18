---
description: Flag capacità driver.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953e73c0ea6b079a6b8f0658790c749b4f30a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305053"
---
# <a name="d3dcaps2"></a>D3DCAPS2

Flag capacità driver.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#definire</td>
<td>Valore</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANAUTOGENMIPMAP</td>
<td>0x40000000L</td>
<td>Il driver è in grado di generare automaticamente mipmap. Per ulteriori informazioni, vedere <a href="automatic-generation-of-mipmaps.md">generazione automatica di mipmap (Direct3D 9)</a>.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANCALIBRATEGAMMA</td>
<td>0x00100000L</td>
<td>Nel sistema è installato un calibratore in grado di regolare automaticamente la rampa gamma, in modo che il risultato sia identico in tutti i sistemi con un calibratore. Per richiamare il calibratore quando si impostano nuovi livelli gamma, usare il flag D3DSGR_CALIBRATE quando si chiama <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>. La calibratura delle rampe gamma comporta un sovraccarico di elaborazione e non deve essere usata di frequente.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANSHARERESOURCE</td>
<td>0x80000000L</td>
<td>Il dispositivo può creare risorse condivisibili. I metodi per la creazione di risorse possono impostare valori non NULL per i parametri <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> . 
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
<td>Il driver è in grado di gestire le risorse. In questi driver D3DPOOL_MANAGED risorse verranno gestite dal driver. Per fare in modo che Direct3D esegua l'override del driver affinché Direct3D gestisca le risorse, usare il flag D3DCREATE_DISABLE_DRIVER_MANAGEMENT quando si chiama <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_DYNAMICTEXTURES</td>
<td>0x20000000L</td>
<td>Il driver supporta le trame dinamiche.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_FULLSCREENGAMMA</td>
<td>0x00020000L</td>
<td>Il driver supporta la regolazione della rampa dinamica gamma in modalità schermo intero.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_RESERVED</td>
<td>0x02000000L</td>
<td>Riservati non utilizzato.</td>
</tr>
</tbody>
</table>



 

Queste costanti vengono usate dal membro D3CAPS2 di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
