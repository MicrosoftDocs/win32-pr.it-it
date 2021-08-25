---
description: Attributi che possono essere recuperati in un elemento (file o cartella) o in un set di elementi.
ms.assetid: 4cb85995-cdc8-4474-8c4d-c783ac91c759
title: SFGAO (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a5ae5dca355b7c22e3075a0ced7640a5bd45a54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481987"
---
# <a name="sfgao"></a>SFGAO

Attributi che possono essere recuperati in un elemento (file o cartella) o in un set di elementi.




| Costante/valore | Descrizione | 
|----------------|-------------|
| <span id="SFGAO_CANCOPY"></span><span id="sfgao_cancopy"></span><dl><dt><strong>SFGAO_CANCOPY</strong></dt><dt>0x00000001</dt></dl> | Gli elementi specificati possono essere copiati.<br /> | 
| <span id="SFGAO_CANMOVE"></span><span id="sfgao_canmove"></span><dl><dt><strong>SFGAO_CANMOVE</strong></dt><dt>0x00000002</dt></dl> | Gli elementi specificati possono essere spostati.<br /> | 
| <span id="SFGAO_CANLINK"></span><span id="sfgao_canlink"></span><dl><dt><strong>SFGAO_CANLINK</strong></dt><dt>0x00000004</dt></dl> | È possibile creare collegamenti per gli elementi specificati. Questo attributo ha lo stesso valore di <a href="/windows/desktop/com/dropeffect-constants"><strong>DROPEFFECT_LINK</strong></a>. <br /> Se un'estensione dello spazio <strong></strong> dei nomi restituisce questo attributo, al menu di scelta rapida visualizzato durante le operazioni di trascinamento della selezione viene aggiunta una voce Crea collegamento con un gestore predefinito. L'estensione può anche implementare il proprio gestore per il <em>verbo di</em> collegamento al posto dell'impostazione predefinita. In questo caso, l'estensione è responsabile della creazione del collegamento.<br /> Un <strong>elemento Crea</strong> collegamento viene aggiunto anche al menu Windows File di Esplora risorse e ai normali menu di scelta rapida. <strong></strong><br /> Se l'elemento è selezionato, il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu::InvokeCommand</strong></a> dell'applicazione viene richiamato con il membro <strong>lpVerb</strong> della struttura <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> impostato per collegare <em>.</em> L'applicazione è responsabile della creazione del collegamento.<br /> | 
| <span id="SFGAO_STORAGE"></span><span id="sfgao_storage"></span><dl><dt><strong>SFGAO_STORAGE</strong></dt><dt>0x00000008</dt></dl> | Gli elementi specificati possono essere associati a un <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>oggetto IStorage</strong></a> tramite <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Per altre informazioni sulle funzionalità di manipolazione dello spazio dei nomi, vedere <strong>IStorage.</strong><br /> | 
| <span id="SFGAO_CANRENAME"></span><span id="sfgao_canrename"></span><dl><dt><strong>SFGAO_CANRENAME</strong></dt><dt>0x00000010</dt></dl> | Gli elementi specificati possono essere rinominati. Si noti che questo valore è essenzialmente un suggerimento. non tutti i client dello spazio dei nomi consentono la ridenominazione degli elementi. Tuttavia, per gli utenti che dispongono di questo attributo è necessario impostare questo attributo.<br /> | 
| <span id="SFGAO_CANDELETE"></span><span id="sfgao_candelete"></span><dl><dt><strong>SFGAO_CANDELETE</strong></dt><dt>0x00000020</dt></dl> | Gli elementi specificati possono essere eliminati.<br /> | 
| <span id="SFGAO_HASPROPSHEET"></span><span id="sfgao_haspropsheet"></span><dl><dt><strong>SFGAO_HASPROPSHEET</strong></dt><dt>0x00000040</dt></dl> | Gli elementi specificati hanno finestre delle proprietà.<br /> | 
| <span id="SFGAO_DROPTARGET"></span><span id="sfgao_droptarget"></span><dl><dt><strong>SFGAO_DROPTARGET</strong></dt><dt>0x00000100</dt></dl> | Gli elementi specificati sono destinazioni di rilascio.<br /> | 
| <span id="SFGAO_CAPABILITYMASK"></span><span id="sfgao_capabilitymask"></span><dl><dt><strong>SFGAO_CAPABILITYMASK</strong></dt><dt>0x00000177</dt></dl> | Questo flag è una maschera per gli attributi di funzionalità: SFGAO_CANCOPY, SFGAO_CANMOVE, SFGAO_CANLINK, SFGAO_CANRENAME, SFGAO_CANDELETE, SFGAO_HASPROPSHEET e SFGAO_DROPTARGET. I chiamanti in genere non usano questo valore.<br /> | 
| <span id="SFGAO_SYSTEM"></span><span id="sfgao_system"></span><dl><dt><strong>SFGAO_SYSTEM</strong></dt><dt>0x00001000</dt></dl> | <strong>Windows 7 e versioni successive.</strong> Gli elementi specificati sono elementi di sistema.<br /> | 
| <span id="SFGAO_ENCRYPTED"></span><span id="sfgao_encrypted"></span><dl><dt><strong>SFGAO_ENCRYPTED</strong></dt><dt>0x00002000</dt></dl> | Gli elementi specificati sono crittografati e potrebbero richiedere una presentazione speciale.<br /> | 
| <span id="SFGAO_ISSLOW"></span><span id="sfgao_isslow"></span><dl><dt><strong>SFGAO_ISSLOW</strong></dt><dt>0x00004000</dt></dl> | L'accesso all'elemento <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>(tramite IStream</strong></a> o altre interfacce di archiviazione) dovrebbe essere un'operazione lenta. Le applicazioni devono evitare di accedere agli elementi contrassegnati con SFGAO_ISSLOW. <br /><blockquote>[!Note]<br />L'apertura di un flusso per un elemento è in genere un'operazione lenta in qualsiasi momento. SFGAO_ISSLOW indica che è previsto che sia particolarmente lento, ad esempio in caso di connessioni di rete lente o di file offline (FILE_ATTRIBUTE_OFFLINE). Tuttavia, l'esecuzione SFGAO_ISSLOW query è a sua stessa un'operazione lenta. Le applicazioni devono eseguire query SFGAO_ISSLOW solo in un thread in background. È possibile usare un metodo alternativo, ad esempio il recupero della proprietà <a href="/windows/desktop/properties/props-system-fileattributes"><strong>PKEY_FileAttributes</strong></a> e il test per FILE_ATTRIBUTE_OFFLINE, al posto di una chiamata al metodo che comporta SFGAO_ISSLOW.</blockquote><br /> | 
| <span id="SFGAO_GHOSTED"></span><span id="sfgao_ghosted"></span><dl><dt><strong>SFGAO_GHOSTED</strong></dt><dt>0x00008000</dt></dl> | Gli elementi specificati vengono visualizzati in grigio e non disponibili per l'utente.<br /> | 
| <span id="SFGAO_LINK"></span><span id="sfgao_link"></span><dl><dt><strong>SFGAO_LINK</strong></dt><dt>0x00010000</dt></dl> | Gli elementi specificati sono collegamenti.<br /> | 
| <span id="SFGAO_SHARE"></span><span id="sfgao_share"></span><dl><dt><strong>SFGAO_SHARE</strong></dt><dt>0x00020000</dt></dl> | Gli oggetti specificati sono condivisi.<br /> | 
| <span id="SFGAO_READONLY"></span><span id="sfgao_readonly"></span><dl><dt><strong>SFGAO_READONLY</strong></dt><dt>0x00040000</dt></dl> | Gli elementi specificati sono di sola lettura. Nel caso delle cartelle, ciò significa che non è possibile creare nuovi elementi in tali cartelle. Questo comportamento non deve essere confuso con il comportamento specificato dal flag FILE_ATTRIBUTE_READONLY recuperato da <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider::GetItemData</strong></a> in una <a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>struttura SHCOLUMNDATA.</strong></a> FILE_ATTRIBUTE_READONLY non ha alcun significato per le cartelle file system Win32.<br /> | 
| <span id="SFGAO_HIDDEN"></span><span id="sfgao_hidden"></span><dl><dt><strong>SFGAO_HIDDEN</strong></dt><dt>0x00080000</dt></dl> | L'elemento è nascosto e non <strong></strong> deve essere visualizzato a meno che l'opzione Mostra cartelle e file nascosti non sia abilitata in <strong>Cartella Impostazioni</strong>.<br /> | 
| <span id="SFGAO_DISPLAYATTRMASK"></span><span id="sfgao_displayattrmask"></span><dl><dt><strong>SFGAO_DISPLAYATTRMASK</strong></dt><dt>0x000FC000</dt></dl> | Non usare.<br /> | 
| <span id="SFGAO_NONENUMERATED"></span><span id="sfgao_nonenumerated"></span><dl><dt><strong>SFGAO_NONENUMERATED</strong></dt><dt>0x00100000</dt></dl> | Gli elementi non sono enumerati e devono essere nascosti. Non vengono restituiti tramite un enumeratore, ad esempio quello creato dal <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>metodo IShellFolder::EnumObjects.</strong></a><br /> | 
| <span id="SFGAO_NEWCONTENT"></span><span id="sfgao_newcontent"></span><dl><dt><strong>SFGAO_NEWCONTENT</strong></dt><dt>0x00200000</dt></dl> | Gli elementi contengono nuovo contenuto, come definito dall'applicazione specifica.<br /> | 
| <span id="SFGAO_CANMONIKER"></span><span id="sfgao_canmoniker"></span><dl><dt><strong>SFGAO_CANMONIKER</strong></dt></dl> | Non supportata.<br /> | 
| <span id="SFGAO_HASSTORAGE"></span><span id="sfgao_hasstorage"></span><dl><dt><strong>SFGAO_HASSTORAGE</strong></dt></dl> | Non supportata.<br /> | 
| <span id="SFGAO_STREAM"></span><span id="sfgao_stream"></span><dl><dt><strong>SFGAO_STREAM</strong></dt><dt>0x00400000</dt></dl> | Indica che all'elemento è associato un flusso. Tale flusso è accessibile tramite una chiamata a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a> con IID_IStream nel <em>parametro riid.</em><br /> | 
| <span id="SFGAO_STORAGEANCESTOR"></span><span id="sfgao_storageancestor"></span><dl><dt><strong>SFGAO_STORAGEANCESTOR</strong></dt><dt>0x00800000</dt></dl> | Gli elementi figlio di questo elemento sono accessibili tramite <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> o <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage.</strong></a> Tali elementi figlio sono contrassegnati con SFGAO_STORAGE o SFGAO_STREAM.<br /> | 
| <span id="SFGAO_VALIDATE"></span><span id="sfgao_validate"></span><dl><dt><strong>SFGAO_VALIDATE</strong></dt><dt>0x01000000</dt></dl> | Se specificato come input, SFGAO_VALIDATE indica alla cartella di convalidare l'esistenza degli elementi contenuti in una cartella o in una matrice di elementi della shell. Se uno o più di questi elementi non esistono, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof"><strong>IShellFolder::GetAttributesOf</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes"><strong>IShellItemArray::GetAttributes</strong></a> restituiscono un codice di errore. Questo flag non viene mai restituito come valore [out].<br /> Se usato con la cartella file system, SFGAO_VALIDATE indica alla cartella di eliminare le proprietà memorizzate nella cache recuperate dai client di <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex"><strong>IShellFolder2::GetDetailsEx</strong></a> che potrebbero essere state accumulate per gli elementi specificati.<br /> | 
| <span id="SFGAO_REMOVABLE"></span><span id="sfgao_removable"></span><dl><dt><strong>SFGAO_REMOVABLE</strong></dt><dt>0x02000000</dt></dl> | Gli elementi specificati si trovano su supporti rimovibili o sono a loro volta dispositivi rimovibili.<br /> | 
| <span id="SFGAO_COMPRESSED"></span><span id="sfgao_compressed"></span><dl><dt><strong>SFGAO_COMPRESSED</strong></dt><dt>0x04000000</dt></dl> | Gli elementi specificati vengono compressi.<br /> | 
| <span id="SFGAO_BROWSABLE"></span><span id="sfgao_browsable"></span><dl><dt><strong>SFGAO_BROWSABLE</strong></dt><dt>0x08000000</dt></dl> | Gli elementi specificati possono essere ospitati all'interno di un Web browser o Windows Explorer.<br /> | 
| <span id="SFGAO_FILESYSANCESTOR"></span><span id="sfgao_filesysancestor"></span><dl><dt><strong>SFGAO_FILESYSANCESTOR</strong></dt><dt>0x10000000</dt></dl> | Le cartelle specificate sono file system o contengono almeno un discendente (figlio, child o versioni successive) che è una cartella file system (SFGAO_FILESYSTEM).<br /> | 
| <span id="SFGAO_FOLDER"></span><span id="sfgao_folder"></span><dl><dt><strong>SFGAO_FOLDER</strong></dt><dt>0x20000000</dt></dl> | Gli elementi specificati sono cartelle. Alcuni elementi possono essere contrassegnati con SFGAO_STREAM e SFGAO_FOLDER, ad esempio un file compresso con un'estensione .zip file. Alcune applicazioni potrebbero includere questo flag durante il test di elementi che sono sia file che contenitori.<br /> | 
| <span id="SFGAO_FILESYSTEM"></span><span id="sfgao_filesystem"></span><dl><dt><strong>SFGAO_FILESYSTEM</strong></dt><dt>0x40000000</dt></dl> | Le cartelle o i file specificati fanno parte del file system, ovvero sono file, directory o directory radice. Si può presumere che i nomi analizzati degli elementi siano percorsi di file system Win32 validi. Questi percorsi possono essere basati su UNC o su lettera di unità.<br /> | 
| <span id="SFGAO_STORAGECAPMASK"></span><span id="sfgao_storagecapmask"></span><dl><dt><strong>SFGAO_STORAGECAPMASK</strong></dt><dt>0x70C50008</dt></dl> | Questo flag è una maschera per gli attributi delle funzionalità di archiviazione: SFGAO_STORAGE, SFGAO_LINK, SFGAO_READONLY, SFGAO_STREAM, SFGAO_STORAGEANCESTOR, SFGAO_FILESYSANCESTOR, SFGAO_FOLDER e SFGAO_FILESYSTEM. I chiamanti in genere non usano questo valore.<br /> | 
| <span id="SFGAO_HASSUBFOLDER"></span><span id="sfgao_hassubfolder"></span><dl><dt><strong>SFGAO_HASSUBFOLDER</strong></dt><dt>0x80000000</dt></dl> | Le cartelle specificate hanno sottocartelle. L SFGAO_HASSUBFOLDER attributo è solo consultivo e può essere restituito dalle implementazioni della cartella shell anche se non contengono sottocartelle. Si noti, tuttavia, che il contrario, ovvero la mancata restituzione SFGAO_HASSUBFOLDER, indica definitivamente che gli oggetti cartella non hanno sottocartelle.<br /> La restituzione SFGAO_HASSUBFOLDER è consigliabile ogni volta che è necessaria una quantità significativa di tempo per determinare se sono presenti sottocartelle. Ad esempio, la shell restituisce sempre SFGAO_HASSUBFOLDER quando una cartella si trova in un'unità di rete.<br /> | 
| <span id="SFGAO_CONTENTSMASK"></span><span id="sfgao_contentsmask"></span><dl><dt><strong>SFGAO_CONTENTSMASK</strong></dt><dt>0x80000000</dt></dl> | Questo flag è una maschera per gli attributi di contenuto, attualmente solo SFGAO_HASSUBFOLDER. I chiamanti in genere non usano questo valore.<br /> | 
| <span id="SFGAO_PKEYSFGAOMASK"></span><span id="sfgao_pkeysfgaomask"></span><dl><dt><strong>SFGAO_PKEYSFGAOMASK</strong></dt><dt>0x81044000</dt></dl> | Maschera utilizzata dalla <a href="/windows/desktop/properties/props-system-sfgaoflags">proprietà PKEY_SFGAOFlags</a> per determinare gli attributi considerati come causa di calcoli lenti o privi di contesto: SFGAO_ISSLOW, SFGAO_READONLY, SFGAO_HASSUBFOLDER e SFGAO_VALIDATE. I chiamanti in genere non usano questo valore.<br /> | 




## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IShellFolder::GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)
</dt> <dt>

[**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)
</dt> <dt>

[**IShellItemArray::GetAttributes**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes)
</dt> </dl>

 

 
