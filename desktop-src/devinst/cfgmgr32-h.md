---
title: 'Cfgmgr32.h '
description: Questa sezione contiene argomenti di riferimento per l'intestazione cfgmgr32. h.
ms.assetid: 73b4b2ec-ce3d-47c1-9b0e-1052f390ae94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ccc2baf458fea5e20842c9bfa60028c2cb8e23
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300586"
---
# <a name="cfgmgr32h"></a>Cfgmgr32.h 

Questa sezione contiene argomenti di riferimento per l'intestazione cfgmgr32. h.

## <a name="in-this-section"></a>Contenuto della sezione



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
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_des"><strong>BUSNUMBER_DES</strong></a><br/></td>
<td>La struttura BUSNUMBER_DES viene usata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo del numero di bus per un'istanza del dispositivo. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_range"><strong>BUSNUMBER_RANGE</strong></a><br/></td>
<td>La struttura di BUSNUMBER_RANGE specifica un elenco di requisiti delle risorse che descrive l'utilizzo del numero di bus per un'istanza del dispositivo. Per ulteriori informazioni sugli elenchi dei requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_resource"><strong>BUSNUMBER_RESOURCE</strong></a><br/></td>
<td>La struttura BUSNUMBER_RESOURCE specifica un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo del numero di bus per un'istanza del dispositivo. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a><br/></td>
<td>La funzione <strong>CM_Add_Empty_Log_Conf</strong> crea una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a>vuota, per un tipo di configurazione e un'istanza del dispositivo specificati, nel computer locale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex"><strong>CM_Add_Empty_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Add_Empty_Log_Conf_Ex</strong> crea una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a>vuota, per un tipo di configurazione e un'istanza del dispositivo specificati, sia nel computer locale che in un computer remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a><br/></td>
<td>La funzione <strong>CM_Add_ID</strong> aggiunge un <a href="/windows-hardware/drivers/install/device-ids">ID dispositivo</a> specificato (se non è già presente) a un elenco di <a href="/windows-hardware/drivers/install/hardware-ids">ID hardware</a> o a un elenco di <a href="/windows-hardware/drivers/install/compatible-ids">ID compatibili</a> di un' <a href="/windows-hardware/drivers/">istanza del dispositivo</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_id_exw"><strong>CM_Add_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Add_ID_Ex</strong> aggiunge un <a href="/windows-hardware/drivers/install/device-ids">ID dispositivo</a> (se non è già presente) a un elenco di <a href="/windows-hardware/drivers/install/hardware-ids">ID hardware</a> dell'istanza del dispositivo o a un elenco di <a href="/windows-hardware/drivers/install/compatible-ids">ID compatibili</a> , sia nel computer locale che in un computer remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a><br/></td>
<td>La funzione <strong>CM_Add_Res_Des</strong> aggiunge un <a href="/windows-hardware/drivers/">descrittore di risorsa</a> a una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex"><strong>CM_Add_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Add_Res_Des_Ex</strong> aggiunge un <a href="/windows-hardware/drivers/">descrittore di risorsa</a> a una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a>. La configurazione logica può trovarsi nel computer locale o in un computer remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_connect_machinew"><strong>CM_Connect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e la funzionalità Windows Server 2012 per accedere ai computer remoti è stata rimossa. Non è possibile accedere ai computer remoti durante l'esecuzione in queste versioni di Windows.
</blockquote>
<br/> La funzione <strong>CM_Connect_Machine</strong> crea una connessione a un computer remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_class_key"><strong>CM_Delete_Class_Key</strong></a><br/></td>
<td>La funzione <strong>CM_Delete_Class_Key</strong> rimuove dal sistema la <a href="/windows-hardware/drivers/">classe del dispositivo</a> installata specificata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a><br/></td>
<td>La funzione <strong>CM_Delete_Device_Interface_Key</strong> Elimina la sottochiave del registro di sistema utilizzata dalle applicazioni e dai driver per archiviare informazioni specifiche dell'interfaccia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exa"><strong>CM_Delete_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Delete_Device_Interface_Key_ExA</strong> Elimina la sottochiave del registro di sistema utilizzata dalle applicazioni e dai driver per archiviare informazioni specifiche dell'interfaccia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exw"><strong>CM_Delete_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Delete_Device_Interface_Key_ExW</strong> Elimina la sottochiave del registro di sistema utilizzata dalle applicazioni e dai driver per archiviare informazioni specifiche dell'interfaccia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_devnode_key"><strong>CM_Delete_DevNode_Key</strong></a><br/></td>
<td>La funzione <strong>CM_Delete_DevNode_Key</strong> Elimina le chiavi del registro di sistema accessibili dall'utente specificate associate a un dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disable_devnode"><strong>CM_Disable_DevNode</strong></a><br/></td>
<td>La funzione <strong>CM_Disable_DevNode</strong> Disabilita un dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disconnect_machine"><strong>CM_Disconnect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e la funzionalità Windows Server 2012 per accedere ai computer remoti è stata rimossa. Non è possibile accedere ai computer remoti durante l'esecuzione in queste versioni di Windows.
</blockquote>
<br/> La funzione <strong>CM_Disconnect_Machine</strong> rimuove una connessione a un computer remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enable_devnode"><strong>CM_Enable_DevNode</strong></a><br/></td>
<td>La funzione <strong>CM_Enable_DevNode</strong> Abilita un dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a><br/></td>
<td>La funzione <strong>CM_Enumerate_Classes</strong> , quando viene chiamata ripetutamente, enumera le <a href="/windows-hardware/drivers/">classi di dispositivi</a> installate del computer locale fornendo il GUID di ogni classe.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes_ex"><strong>CM_Enumerate_Classes_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Enumerate_Classes_Ex</strong> , quando viene chiamata ripetutamente, enumera <a href="/windows-hardware/drivers/">le classi di dispositivi</a>installate di un computer locale o remoto, fornendo il GUID di ogni classe.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a><br/></td>
<td>La funzione <strong>CM_Enumerate_Enumerators</strong> enumera gli enumeratori dei dispositivi del computer locale specificando il nome di ogni enumeratore.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumerators_exw"><strong>CM_Enumerate_Enumerators_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Enumerate_Enumerators_Ex</strong> enumera gli enumeratori di dispositivo di un computer locale o remoto, specificando il nome di ogni enumeratore.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a><br/></td>
<td>La funzione <strong>CM_Free_Log_Conf</strong> rimuove una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a> e tutti i <a href="/windows-hardware/drivers/">descrittori di risorse</a> associati dal computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex"><strong>CM_Free_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Free_Log_Conf_Ex</strong> rimuove una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a> e tutti i <a href="/windows-hardware/drivers/">descrittori di risorse</a> associati da un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle"><strong>CM_Free_Log_Conf_Handle</strong></a><br/></td>
<td>La funzione <strong>CM_Free_Log_Conf_Handle</strong> invalida un handle di configurazione logica e libera l'allocazione di memoria associata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a><br/></td>
<td>La funzione <strong>CM_Free_Res_Des</strong> rimuove un <a href="/windows-hardware/drivers/">descrittore di risorsa</a> da una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a> nel computer locale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_ex"><strong>CM_Free_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Free_Res_Des_Ex</strong> rimuove un <a href="/windows-hardware/drivers/">descrittore di risorsa</a> da una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a> in un computer locale o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle"><strong>CM_Free_Res_Des_Handle</strong></a><br/></td>
<td>La funzione <strong>CM_Free_Res_Des_Handle</strong> invalida una descrizione della risorsa handle e libera l'allocazione di memoria associata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_resource_conflict_handle"><strong>CM_Free_Resource_Conflict_Handle</strong></a><br/></td>
<td>La funzione <strong>CM_Free_Resource_Conflict_Handle</strong> invalida un handle per un elenco di conflitti di risorse e libera l'allocazione di memoria associata all'handle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Child</strong> viene usata per recuperare un handle di istanza di dispositivo al primo nodo figlio di un nodo di dispositivo specificato (<a href="/windows-hardware/drivers/">devnode</a>) nell'albero dei <a href="/windows-hardware/drivers/kernel/device-tree">dispositivi</a>del computer locale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child_ex"><strong>CM_Get_Child_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Child_Ex</strong> viene usata per recuperare un handle di istanza del dispositivo al primo nodo figlio di un nodo di dispositivo specificato (<a href="/windows-hardware/drivers/">devnode</a>) in un <a href="/windows-hardware/drivers/kernel/device-tree">albero dei dispositivi</a>di un computer locale o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Class_Property</strong> recupera una proprietà del dispositivo impostata per una classe di <a href="/windows-hardware/drivers/install/device-interface-classes">interfaccia del dispositivo</a> o una classe di installazione del <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_exw"><strong>CM_Get_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Class_Property_ExW</strong> recupera una proprietà del dispositivo impostata per una classe di <a href="/windows-hardware/drivers/install/device-interface-classes">interfaccia del dispositivo</a> o una classe di installazione del <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivo</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Class_Property_Keys</strong> recupera una matrice delle chiavi delle proprietà del dispositivo che rappresentano le proprietà del dispositivo impostate per una classe di <a href="/windows-hardware/drivers/install/device-interface-classes">interfaccia del dispositivo</a> o una classe di installazione del <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys_ex"><strong>CM_Get_Class_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Class_Property_Keys_Ex</strong> recupera una matrice delle chiavi delle proprietà del dispositivo che rappresentano le proprietà del dispositivo impostate per una classe di <a href="/windows-hardware/drivers/install/device-interface-classes">interfaccia del dispositivo</a> o una classe di installazione del <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivo</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw"><strong>CM_Get_Class_Registry_Property</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Class_Registry_Property</strong> recupera una <a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">proprietà della classe di installazione del dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Depth</strong> viene utilizzata per ottenere la profondità di un nodo di dispositivo specificato (<a href="/windows-hardware/drivers/">devnode</a>) all'interno dell' <a href="/windows-hardware/drivers/kernel/device-tree">albero del dispositivo</a>del computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth_ex"><strong>CM_Get_Depth_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Depth_Ex</strong> viene utilizzata per ottenere la profondità di un nodo di dispositivo specificato (<a href="/windows-hardware/drivers/">devnode</a>) all'interno di un <a href="/windows-hardware/drivers/kernel/device-tree">albero di dispositivi</a>di un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Device_ID</strong> recupera l' <a href="/windows-hardware/drivers/install/device-instance-ids">ID dell'istanza del dispositivo</a> per un' <a href="/windows-hardware/drivers/">istanza del dispositivo</a> specificata nel computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_exw"><strong>CM_Get_Device_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Device_ID_Ex</strong> recupera l' <a href="/windows-hardware/drivers/install/device-instance-ids">ID dell'istanza del dispositivo</a> per un' <a href="/windows-hardware/drivers/">istanza del dispositivo</a> specificata in un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Device_ID_List</strong> recupera un elenco di <a href="/windows-hardware/drivers/install/device-instance-ids">ID istanza dispositivo</a> per le <a href="/windows-hardware/drivers/">istanze del dispositivo</a>del computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exw"><strong>CM_Get_Device_ID_List_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Device_ID_List_Ex</strong> recupera un elenco di <a href="/windows-hardware/drivers/install/device-instance-ids">ID istanza dispositivo</a> per le <a href="/windows-hardware/drivers/">istanze del dispositivo</a> in un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Device_ID_List_Size</strong> recupera le dimensioni del buffer necessarie per memorizzare un elenco di <a href="/windows-hardware/drivers/install/device-instance-ids">ID istanza del dispositivo</a> per le istanze del <a href="/windows-hardware/drivers/">dispositivo</a>del computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw"><strong>CM_Get_Device_ID_List_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Device_ID_List_Size_Ex</strong> recupera le dimensioni del buffer necessarie per memorizzare un elenco di <a href="/windows-hardware/drivers/install/device-instance-ids">ID istanza dispositivo</a> per le <a href="/windows-hardware/drivers/">istanze di dispositivo</a>di un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Device_ID_Size</strong> recupera le dimensioni del buffer necessarie per memorizzare l' <a href="/windows-hardware/drivers/install/device-instance-ids">ID</a> di un'istanza <a href="/windows-hardware/drivers/">del dispositivo nel computer</a> locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex"><strong>CM_Get_Device_ID_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Device_ID_Size_Ex</strong> recupera le dimensioni del buffer necessarie per conservare l' <a href="/windows-hardware/drivers/install/device-instance-ids">ID</a> di un'istanza del <a href="/windows-hardware/drivers/">dispositivo in un</a> computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_aliasw"><strong>CM_Get_Device_Interface_Alias</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Device_Interface_Alias</strong> restituisce l'alias dell'istanza di interfaccia del dispositivo specificata, se l'alias esiste.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Device_Interface_List</strong> recupera un elenco di istanze di interfaccia del dispositivo che appartengono a una <a href="/windows-hardware/drivers/install/device-interface-classes">classe di interfaccia del dispositivo</a>specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea"><strong>CM_Get_Device_Interface_List_Size</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Device_Interface_List_Size</strong> recupera le dimensioni del buffer che devono essere passate alla funzione di <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Device_Interface_Property</strong> recupera una proprietà del dispositivo impostata per un'interfaccia del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_exw"><strong>CM_Get_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Device_Interface_Property_ExW</strong> recupera una proprietà del dispositivo impostata per un'interfaccia del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Device_Interface_Property_Keys</strong> recupera una matrice di chiavi di proprietà del dispositivo che rappresentano le proprietà del dispositivo impostate per un'interfaccia del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keys_exw"><strong>CM_Get_Device_Interface_Property_Keys_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Device_Interface_Property_Keys_ExW</strong> recupera una matrice di chiavi di proprietà del dispositivo che rappresentano le proprietà del dispositivo impostate per un'interfaccia del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a><br/></td>
<td>La funzione <strong>CM_Get_DevNode_Property</strong> recupera una proprietà dell'istanza del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_exw"><strong>CM_Get_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_DevNode_Property_ExW</strong> recupera una proprietà dell'istanza del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a><br/></td>
<td>La funzione <strong>CM_Get_DevNode_Property_Keys</strong> recupera una matrice delle chiavi delle proprietà del dispositivo che rappresentano le proprietà del dispositivo impostate per un'istanza del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys_ex"><strong>CM_Get_DevNode_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_DevNode_Property_Keys_Ex</strong> recupera una matrice delle chiavi delle proprietà del dispositivo che rappresentano le proprietà del dispositivo impostate per un'istanza del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_registry_propertyw"><strong>CM_Get_DevNode_Registry_Property</strong></a><br/></td>
<td>La funzione <strong>CM_Get_DevNode_Registry_Property</strong> recupera una proprietà del dispositivo specificata dal registro di sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a><br/></td>
<td>La funzione <strong>CM_Get_DevNode_Status</strong> ottiene lo stato di un'istanza del dispositivo dal relativo nodo del dispositivo (<a href="/windows-hardware/drivers/">devnode</a>) nell' <a href="/windows-hardware/drivers/kernel/device-tree">albero del dispositivo</a>del computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex"><strong>CM_Get_DevNode_Status_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_DevNode_Status_Ex</strong> ottiene lo stato di un'istanza del dispositivo dal relativo nodo del dispositivo (<a href="/windows-hardware/drivers/">devnode</a>) in un <a href="/windows-hardware/drivers/kernel/device-tree">albero del dispositivo</a>locale o in un computer remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a><br/></td>
<td>La funzione <strong>CM_Get_First_Log_Conf</strong> ottiene la prima <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a>, di un tipo di configurazione specificato, associata a un'istanza del <a href="/windows-hardware/drivers/">dispositivo</a> specificata nel computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex"><strong>CM_Get_First_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_First_Log_Conf_Ex</strong> ottiene la prima <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a> associata a un'istanza di <a href="/windows-hardware/drivers/">dispositivo</a> specificata in un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsa"><strong>CM_Get_HW_Prof_Flags</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata e non deve essere usata.
</blockquote>
<br/> La funzione <strong>CM_Get_HW_Prof_Flags</strong> recupera i flag di configurazione specifici del <a href="/windows-hardware/drivers/">profilo hardware</a>per un' <a href="/windows-hardware/drivers/">istanza del dispositivo</a> in un computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flags_exa"><strong>CM_Get_HW_Prof_Flags_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è stata deprecata e non deve essere utilizzata.
</blockquote>
<br/> La funzione <strong>CM_Get_HW_Prof_Flags_Ex</strong> recupera i flag di configurazione specifici del <a href="/windows-hardware/drivers/">profilo hardware</a>per un' <a href="/windows-hardware/drivers/">istanza del dispositivo</a> in un computer remoto o in un computer locale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Log_Conf_Priority</strong> ottiene la priorità di configurazione di una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a> specificata nel computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority_ex"><strong>CM_Get_Log_Conf_Priority_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Log_Conf_Priority_Ex</strong> ottiene la priorità di configurazione di una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a> specificata in un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Next_Log_Conf</strong> ottiene la successiva <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a> associata a una specifica istanza del <a href="/windows-hardware/drivers/">dispositivo</a> nel computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex"><strong>CM_Get_Next_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Next_Log_Conf_Ex</strong> ottiene la successiva <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a> associata a una specifica istanza del <a href="/windows-hardware/drivers/">dispositivo</a> in un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Next_Res_Des</strong> ottiene un handle per il <a href="/windows-hardware/drivers/">descrittore di risorsa</a>successivo, di un tipo di risorsa specificato, per una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a> nel computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex"><strong>CM_Get_Next_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Next_Res_Des_Ex</strong> ottiene un handle per il <a href="/windows-hardware/drivers/">descrittore di risorsa</a>successivo, di un tipo di risorsa specificato, per una <a href="/windows-hardware/drivers/kernel/hardware-resources">configurazione logica</a> in un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Parent</strong> ottiene un handle di istanza di dispositivo per il nodo padre di un nodo di dispositivo specificato (<a href="/windows-hardware/drivers/">devnode</a>) nell'albero del dispositivo del computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent_ex"><strong>CM_Get_Parent_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Parent_Ex</strong> ottiene un handle di istanza di dispositivo per il nodo padre di un nodo di dispositivo specificato (<a href="/windows-hardware/drivers/">devnode</a>) in un <a href="/windows-hardware/drivers/kernel/device-tree">albero del dispositivo</a>del computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Res_Des_Data</strong> recupera le informazioni archiviate in un <a href="/windows-hardware/drivers/">descrittore di risorse</a> nel computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex"><strong>CM_Get_Res_Des_Data_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Res_Des_Data_Ex</strong> recupera le informazioni archiviate in un <a href="/windows-hardware/drivers/">descrittore di risorse</a> in un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Res_Des_Data_Size</strong> ottiene le dimensioni del buffer necessarie per contenere le informazioni contenute in un <a href="/windows-hardware/drivers/">descrittore di risorse</a> specificato nel computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size_ex"><strong>CM_Get_Res_Des_Data_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Res_Des_Data_Size_Ex</strong> ottiene le dimensioni del buffer necessarie per contenere le informazioni contenute in un <a href="/windows-hardware/drivers/">descrittore di risorse</a> specificato in un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count"><strong>CM_Get_Resource_Conflict_Count</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Resource_Conflict_Count</strong> ottiene il numero di conflitti contenuti in un elenco di conflitti di risorse specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Resource_Conflict_Details</strong> ottiene i dettagli relativi a uno dei conflitti di risorse in un elenco di conflitti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a><br/></td>
<td>La funzione <strong>CM_Get_Sibling</strong> ottiene un handle di istanza di dispositivo al nodo di pari livello successivo di un nodo di dispositivo specificato (<a href="/windows-hardware/drivers/">devnode</a>) nell' <a href="/windows-hardware/drivers/kernel/device-tree">albero del dispositivo</a>del computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex"><strong>CM_Get_Sibling_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Get_Sibling_Ex</strong> ottiene un handle di istanza di dispositivo al nodo di pari livello successivo di un nodo di dispositivo specificato, in un <a href="/windows-hardware/drivers/kernel/device-tree">albero di dispositivi</a>locale o in un computer remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version"><strong>CM_Get_Version</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata e non deve essere usata.
</blockquote>
<br/> La funzione <strong>CM_Get_Version</strong> restituisce la versione 4,0 della <a href="/windows-hardware/drivers/">dll</a> Configuration Manager (PnP) Plug and Play (<em>Cfgmgr32.dll</em>) per un computer locale. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version_ex"><strong>CM_Get_Version_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata e non deve essere usata.
</blockquote>
<br/> La funzione <strong>CM_Get_Version_Ex</strong> restituisce la versione 4,0 della <a href="/windows-hardware/drivers/">dll</a> Configuration Manager (PnP) Plug and Play (<em>Cfgmgr32.dll</em>) per un computer locale o remoto. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a><br/></td>
<td>La funzione <strong>CM_Is_Dock_Station_Present</strong> indica se una <a href="/windows-hardware/drivers/">stazione di ancoraggio</a> è presente in un computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex"><strong>CM_Is_Dock_Station_Present_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Is_Dock_Station_Present_Ex</strong> indica se una <a href="/windows-hardware/drivers/">stazione di ancoraggio</a> è presente in un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available"><strong>CM_Is_Version_Available</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata e non deve essere usata.
</blockquote>
<br/> La funzione <strong>CM_Is_Version_Available</strong> indica se una versione specificata di plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) è supportata da un computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex"><strong>CM_Is_Version_Available_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata e non deve essere usata.
</blockquote>
<br/> La funzione <strong>CM_Is_Version_Available_Ex</strong> indica se una versione specificata di plug and Play (PNP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) è supportata da un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a><br/></td>
<td>La funzione <strong>CM_Locate_DevNode</strong> ottiene un handle di istanza di dispositivo al nodo del dispositivo associato a un ID di <a href="/windows-hardware/drivers/install/device-instance-ids">istanza del dispositivo</a> specificato nel computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw"><strong>CM_Locate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Locate_DevNode_Ex</strong> ottiene un handle di istanza di dispositivo al nodo del dispositivo associato a un ID di <a href="/windows-hardware/drivers/install/device-instance-ids">istanza del dispositivo</a>specificato, in un computer locale o in un computer remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_mapcrtowin32err"><strong>CM_MapCrToWin32Err</strong></a><br/></td>
<td>Converte un codice <strong>CONFIGRET</strong> specificato nel codice di errore di sistema equivalente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a><br/></td>
<td>La funzione <strong>CM_Modify_Res_Des</strong> modifica un descrittore di risorsa specificato nel computer locale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex"><strong>CM_Modify_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Modify_Res_Des_Ex</strong> modifica un descrittore di risorse specificato in un computer locale o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ne-cfgmgr32-cm_notify_action"><strong>CM_NOTIFY_ACTION</strong></a><br/></td>
<td>Questa enumerazione identifica Plug and Play tipi di evento del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_event_data"><strong>CM_NOTIFY_EVENT_DATA</strong></a><br/></td>
<td>Si tratta di una struttura di dati degli eventi di notifica del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_filter"><strong>CM_NOTIFY_FILTER</strong></a><br/></td>
<td>Struttura filtro notifiche dispositivo<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_class_keyw"><strong>CM_Open_Class_Key</strong></a><br/></td>
<td>La funzione <strong>CM_Open_Class_Key</strong> apre la chiave del registro di sistema della classe di installazione del dispositivo, la chiave del registro di sistema della classe dell'interfaccia del dispositivo o una sottochiave specifica di una classe<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a><br/></td>
<td>La funzione <strong>CM_Open_Device_Interface_Key</strong> apre la sottochiave del registro di sistema utilizzata dalle applicazioni e dai driver per archiviare le informazioni specifiche di un'interfaccia del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keya"><strong>CM_Open_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Open_Device_Interface_Key_ExA</strong> apre la sottochiave del registro di sistema utilizzata dalle applicazioni e dai driver per archiviare le informazioni specifiche di un'interfaccia del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_key_exw"><strong>CM_Open_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Open_Device_Interface_Key_ExW</strong> apre la sottochiave del registro di sistema utilizzata dalle applicazioni e dai driver per archiviare le informazioni specifiche di un'interfaccia del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_devnode_key"><strong>CM_Open_DevNode_Key</strong></a><br/></td>
<td>La funzione <strong>CM_Open_DevNode_Key</strong> apre una chiave del registro di sistema per le informazioni di configurazione specifiche del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a><br/></td>
<td>La funzione <strong>CM_Query_And_Remove_SubTree</strong> controlla se un'istanza del dispositivo e i relativi elementi figlio possono essere rimossi e, in caso affermativo, li rimuove.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw"><strong>CM_Query_And_Remove_SubTree_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Query_And_Remove_SubTree_Ex</strong> controlla se un'istanza del dispositivo e i relativi elementi figlio possono essere rimossi e, in caso affermativo, li rimuove.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list"><strong>CM_Query_Resource_Conflict_List</strong></a><br/></td>
<td>La funzione <strong>CM_Query_Resource_Conflict_List</strong> identifica le istanze del dispositivo con requisiti di risorse in conflitto con la descrizione della risorsa di un'istanza del dispositivo specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a><br/></td>
<td>La funzione <strong>CM_Reenumerate_DevNode</strong> enumera i dispositivi identificati da un nodo del dispositivo specificato e da tutti i relativi elementi figlio.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode_ex"><strong>CM_Reenumerate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Reenumerate_DevNode_Ex</strong> enumera i dispositivi identificati da un nodo del dispositivo specificato e da tutti i relativi elementi figlio.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a><br/></td>
<td>Usare <a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa"><strong>RegisterDeviceNotification</strong></a> invece di <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> se il codice è destinato a Windows 7 o alle versioni precedenti di Windows. I chiamanti in modalità kernel devono invece usare <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-ioregisterplugplaynotification"><strong>IoRegisterPlugPlayNotification</strong></a> .<br/> La funzione <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> registra una routine di callback dell'applicazione da chiamare quando si verifica un evento PNP del tipo specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a><br/></td>
<td>La funzione <strong>CM_Request_Device_Eject</strong> prepara un'istanza del dispositivo locale per la rimozione sicura, se il dispositivo è rimovibile. Se il dispositivo può essere espulso fisicamente, sarà.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw"><strong>CM_Request_Device_Eject_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Request_Device_Eject_Ex</strong> prepara un'istanza locale o remota del dispositivo per la rimozione sicura, se il dispositivo è rimovibile. Se il dispositivo può essere espulso fisicamente, sarà.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a><br/></td>
<td>La funzione <strong>CM_Request_Eject_PC</strong> richiede che un PC portatile, inserito in una <a href="/windows-hardware/drivers/">stazione di ancoraggio</a>locale, venga espulso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex"><strong>CM_Request_Eject_PC_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Request_Eject_PC_Ex</strong> richiede che un PC portatile, inserito in una <a href="/windows-hardware/drivers/">stazione di ancoraggio</a>locale o remota, venga espulso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a><br/></td>
<td>La funzione <strong>CM_Set_Class_Property</strong> imposta una proprietà della classe per una classe di installazione del dispositivo o una classe di interfaccia del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_property_exw"><strong>CM_Set_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Set_Class_Property_ExW</strong> imposta una proprietà della classe per una classe di installazione del dispositivo o una classe di interfaccia del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_registry_propertyw"><strong>CM_Set_Class_Registry_Property</strong></a><br/></td>
<td>La funzione <strong>CM_Set_Class_Registry_Property</strong> imposta o Elimina una proprietà di una <a href="/windows-hardware/drivers/install/device-setup-classes">classe di installazione del dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a><br/></td>
<td>La funzione <strong>CM_Set_Device_Interface_Property</strong> imposta una proprietà del dispositivo di un'interfaccia del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_property_exw"><strong>CM_Set_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Set_Device_Interface_Property_ExW</strong> imposta una proprietà del dispositivo di un'interfaccia del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a><br/></td>
<td>La funzione <strong>CM_Set_DevNode_Problem</strong> imposta un codice problema per un dispositivo installato in un computer locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex"><strong>CM_Set_DevNode_Problem_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Set_DevNode_Problem_Ex</strong> imposta un codice problema per un dispositivo installato in un computer locale o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a><br/></td>
<td>La funzione <strong>CM_Set_DevNode_Property</strong> imposta una proprietà dell'istanza del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_property_exw"><strong>CM_Set_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partire da Windows 8 e Windows Server 2012, questa funzione è stata deprecata. Usare invece <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a> .
</blockquote>
<br/> La funzione <strong>CM_Set_DevNode_Property_ExW</strong> imposta una proprietà dell'istanza del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw"><strong>CM_Set_DevNode_Registry_Property</strong></a><br/></td>
<td>La funzione <strong>CM_Set_DevNode_Registry_Property</strong> imposta una proprietà del dispositivo specificata nel registro di sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_setup_devnode"><strong>CM_Setup_DevNode</strong></a><br/></td>
<td>La funzione <strong>CM_Setup_DevNode</strong> riavvia un'istanza del dispositivo che non è in esecuzione a causa di un problema con la configurazione del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_uninstall_devnode"><strong>CM_Uninstall_DevNode</strong></a><br/></td>
<td>La funzione <strong>CM_Uninstall_DevNode</strong> rimuove tutto lo stato persistente associato a un'istanza del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_unregister_notification"><strong>CM_Unregister_Notification</strong></a><br/></td>
<td>Usare <a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification"><strong>UnregisterDeviceNotification</strong></a> invece di <strong>CM_Unregister_Notification</strong> se il codice è destinato a Windows 7 o alle versioni precedenti di Windows.<br/> La funzione <strong>CM_Unregister_Notification</strong> chiude l'handle HCMNOTIFICATION specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_waitnopendinginstallevents"><strong>CMP_WaitNoPendingInstallEvents</strong></a><br/></td>
<td>La funzione <strong>CMP_WaitNoPendingInstallEvents</strong> attende fino a quando non sono presenti attività di installazione del dispositivo in sospeso per l'esecuzione di gestione PNP.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-conflict_details_a"><strong>CONFLICT_DETAILS</strong></a><br/></td>
<td>La struttura CONFLICT_DETAILS viene utilizzata come parametro per la funzione di <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_des"><strong>CS_DES</strong></a><br/></td>
<td>La struttura CS_DES viene usata per specificare un elenco di risorse che descrive l'utilizzo delle risorse specifiche della classe del dispositivo per un'istanza del dispositivo. Per altre informazioni sugli elenchi di risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_resource"><strong>CS_RESOURCE</strong></a><br/></td>
<td>La struttura CS_RESOURCE viene usata per specificare un elenco di risorse che descrive l'utilizzo delle risorse specifiche della classe del dispositivo per un'istanza del dispositivo. Per altre informazioni sugli elenchi di risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_des"><strong>DMA_DES</strong></a><br/></td>
<td>La struttura DMA_DES viene usata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo del canale DMA (Direct Memory Access) per un'istanza del dispositivo. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_range"><strong>DMA_RANGE</strong></a><br/></td>
<td>La struttura di DMA_RANGE specifica un elenco di requisiti delle risorse che descrive l'utilizzo del canale DMA per un'istanza del dispositivo. Per ulteriori informazioni sugli elenchi dei requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_resource"><strong>DMA_RESOURCE</strong></a><br/></td>
<td>La struttura DMA_RESOURCE viene usata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo del canale DMA per un'istanza del dispositivo. Per ulteriori informazioni sull'elenco di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_des"><strong>IO_DES</strong></a><br/></td>
<td>La struttura IO_DES viene utilizzata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo della porta di I/O per un'istanza del dispositivo. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_range"><strong>IO_RANGE</strong></a><br/></td>
<td>La struttura di IO_RANGE specifica un elenco di requisiti delle risorse che descrive l'utilizzo della porta di I/O per un'istanza del dispositivo. Per ulteriori informazioni sugli elenchi dei requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_resource"><strong>IO_RESOURCE</strong></a><br/></td>
<td>La struttura IO_RESOURCE viene utilizzata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo della porta di I/O per un'istanza del dispositivo. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_des_64"><strong>IRQ_DES</strong></a><br/></td>
<td>La struttura IRQ_DES viene usata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo della linea IRQ per un'istanza del dispositivo. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_range"><strong>IRQ_RANGE</strong></a><br/></td>
<td>La struttura di IRQ_RANGE specifica un elenco di requisiti delle risorse che descrive l'utilizzo della linea IRQ per un'istanza del dispositivo. Per ulteriori informazioni sugli elenchi dei requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_resource_64"><strong>IRQ_RESOURCE</strong></a><br/></td>
<td>La struttura IRQ_RESOURCE viene usata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo della linea IRQ per un'istanza del dispositivo. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_des"><strong>MEM_DES</strong></a><br/></td>
<td>La struttura MEM_DES viene usata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo della memoria per un'istanza del dispositivo. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_range"><strong>MEM_RANGE</strong></a><br/></td>
<td>La struttura di MEM_RANGE specifica un elenco di requisiti delle risorse che descrive l'utilizzo della memoria per un'istanza del dispositivo. Per ulteriori informazioni sugli elenchi dei requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_resource"><strong>MEM_RESOURCE</strong></a><br/></td>
<td>La struttura MEM_RESOURCE viene usata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo della memoria per un'istanza del dispositivo. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_des"><strong>MFCARD_DES</strong></a><br/></td>
<td>La struttura MFCARD_DES viene utilizzata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo delle risorse da parte di <em>una</em> delle funzioni hardware fornite da un'istanza di un dispositivo multifunzione. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_resource"><strong>MFCARD_RESOURCE</strong></a><br/></td>
<td>La struttura MFCARD_RESOURCE viene utilizzata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo delle risorse da parte di <em>una</em> delle funzioni hardware fornite da un'istanza di un dispositivo multifunzione. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_des"><strong>PCCARD_DES</strong></a><br/></td>
<td>La struttura PCCARD_DES viene utilizzata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo delle risorse da parte di un'istanza della scheda PC. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_resource"><strong>PCCARD_RESOURCE</strong></a><br/></td>
<td>La struttura PCCARD_RESOURCE viene utilizzata per specificare un elenco di risorse o un elenco di requisiti delle risorse che descrive l'utilizzo delle risorse da parte di un'istanza della scheda PC. Per altre informazioni sugli elenchi di risorse e sugli elenchi di requisiti delle risorse, vedere <a href="/windows-hardware/drivers/kernel/hardware-resources">risorse hardware</a>.<br/></td>
</tr>
</tbody>
</table>



 

 

 

[Invia commenti su questo argomento a Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Cfgmgr32.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Invia commenti su questo argomento a Microsoft")