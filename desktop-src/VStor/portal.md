---
description: Incapsulare il disco rigido in un singolo file per l'uso da parte del sistema operativo come disco virtuale. I dischi virtuali possono fungere da dischi di avvio e possono ospitare file System nativi (NTFS, FAT, exFAT e UDF), supportando al tempo stesso le operazioni standard su disco e file.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Disco virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044145f5d631b878b533bbd409fad5eda5b4863f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226106"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Disco virtuale

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Scopo

Il formato del disco rigido virtuale (VHD) è una specifica del formato di immagine disponibile pubblicamente che specifica un disco rigido virtuale incapsulato in un singolo file, in grado di ospitare file System nativi, supportando al contempo operazioni standard su disco e file. Un esempio di come vengono usati i file VHD è la funzionalità [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) in windows Server 2008, Virtual Server e Windows Virtual PC. Questi prodotti usano dischi rigidi virtuali per contenere l'immagine del sistema operativo Windows usata da una macchina virtuale come disco di avvio del sistema.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Sviluppatori

Il Software Development Kit (SDK) di Microsoft Windows integra il supporto VHD nativo per l'utilizzo di VHD, semplificando la creazione, la gestione e la distribuzione di immagini Windows nei VHD tramite gli strumenti di supporto o di gestione delle API della piattaforma. Non è necessario installare applicazioni separate o implementare un parser di formato VHD per abilitare queste operazioni. Queste API consentono l'uso generico di dischi rigidi virtuali indipendentemente da qualsiasi altra tecnologia di virtualizzazione.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Requisiti di runtime

VHD è supportato in Windows 7 e Windows Server 2008 R2.

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
<td><p><a href="about-vhd.md">Informazioni su VHD</a></p></td>
<td><p>Descrive il formato VHD con suggerimenti e suggerimenti sull'utilizzo dell'API.</p></td>
</tr>
<tr class="even">
<td><p><a href="vhd-reference.md">Riferimento al disco rigido virtuale</a></p></td>
<td><p>Descrive le funzioni, le strutture e le enumerazioni dell'API VHD.</p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Argomenti correlati

[Servizio dischi virtuali](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
