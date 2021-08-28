---
description: Incapsulare il disco rigido in un singolo file per l'uso da parte del sistema operativo come disco virtuale. I dischi virtuali possono funzionare come dischi di avvio e possono ospitare file system nativi (NTFS, FAT, exFAT e UDFS) supportando al tempo stesso operazioni su dischi e file standard.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Disco virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b297ee4a91bd4512cfd38faa5e8a0a5198c8b39a5e66ead26c247f49826d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842112"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Disco virtuale

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Scopo

Il formato VHD (Virtual Hard Disk) è una specifica di formato di immagine disponibile pubblicamente che specifica un disco rigido virtuale incapsulato in un singolo file, in grado di ospitare file system nativi, supportando al tempo stesso operazioni su disco e file standard. Un esempio di come vengono usati i file VHD è la funzionalità [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) in Windows Server 2008, Virtual Server e Windows Virtual PC. Questi prodotti usano dischi rigidi virtuali per contenere Windows'immagine del sistema operativo utilizzata da una macchina virtuale come disco di avvio del sistema.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Sviluppatori

Microsoft Windows Software Development Kit (SDK) integra il supporto VHD nativo per l'uso dei dischi rigidi virtuali, semplificando la creazione, la gestione e la distribuzione di immagini Windows nei dischi rigidi virtuali tramite il supporto api della piattaforma o gli strumenti di gestione. Non è necessario installare applicazioni separate o implementare un parser di formato VHD per abilitare queste operazioni. Queste API consentono l'uso generico dei dischi rigidi virtuali indipendentemente da qualsiasi altra tecnologia di virtualizzazione.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Requisiti di runtime

Il disco rigido virtuale è supportato Windows 7 e Windows Server 2008 R2.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In questa sezione

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="about-vhd.md">Informazioni sul disco rigido virtuale</a></p></td>
<td><p>Descrive il formato del disco rigido virtuale con suggerimenti e suggerimenti per l'utilizzo dell'API.</p></td>
</tr>
<tr class="even">
<td><p><a href="vhd-reference.md">Informazioni di riferimento sul disco rigido virtuale</a></p></td>
<td><p>Descrive le funzioni, le strutture e le enumerazioni dell'API VHD.</p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Argomenti correlati

[Servizio dischi virtuali](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
