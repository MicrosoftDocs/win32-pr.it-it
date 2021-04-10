---
title: Using RC (The RC Command Line) (Uso di RC - Riga di comando RC)
description: Per avviare RC, utilizzare il comando seguente.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963010"
---
# <a name="using-rc-the-rc-command-line"></a>Using RC (The RC Command Line) (Uso di RC - Riga di comando RC)

Per avviare RC, utilizzare il comando seguente.

**RC** \[ *Opzioni* \] di *script-file*

Il parametro *script-file* specifica il nome del file di definizione delle risorse che contiene i nomi, i tipi, i nomi di file e le descrizioni delle risorse da compilare.

RC può generare file di risorse separati per le applicazioni che dispongono di risorse sia indipendenti dalla lingua che specifiche della lingua. Gli sviluppatori possono usare un [file di configurazione delle risorse](/windows/desktop/Intl/preparing-resources) o impostare le opzioni della riga di comando per selezionare i tipi di risorse e gli elementi che sono risorse non localizzabili del [file indipendente dalla lingua](/windows/desktop/Intl/mui-resource-management) e che sono risorse localizzabili dei file MUI specifici della lingua. Per ulteriori informazioni, vedere l' [interfaccia utente multilingue](/windows/desktop/Intl/multilingual-user-interface).

Il parametro *options* può essere costituito da una o più delle seguenti opzioni della riga di comando.

## <a name="options"></a>Opzioni

<dl> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Visualizza un elenco di opzioni della riga di comando.

</dd> <dt>

<span id="_c"></span><span id="_C"></span>**/c**
</dt> <dd>

Definisce una tabella codici utilizzata dalla conversione NLS.

</dd> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Definisce un simbolo per il preprocessore che è possibile testare con la direttiva [**\# ifdef**](-ifdef.md) .

</dd> <dt>

<span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span> *mresname* /FM
</dt> <dd>

RC crea una lingua indipendente dalla lingua. File RES e uno dipendente dalla lingua (MUI). File RES tramite *script-file*. Questa opzione deve essere usata insieme all'opzione **/fo** *resName* RC assegna un nome indipendente dalla lingua. RES file *resName. res* e assegna un nome al linguaggio MUI. File RES *mresname. res*.

**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le funzioni [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.

</dd> <dt>

<span id="_fo_resname"></span><span id="_FO_RESNAME"></span> *resName* /fo
</dt> <dd>

RC crea un oggetto. File RES denominato *resName* con *script-file*.

Se viene impostata anche l'opzione **/FM** *mresname* , RC crea una lingua indipendente dalla lingua. File RES e uno dipendente dalla lingua (MUI). File RES.

**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le funzioni [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.

</dd> <dt>

<span id="_g1"></span><span id="_G1"></span>**/G1**
</dt> <dd>

Se/G1 è impostato, RC genera un file MUI se l'unica risorsa localizzabile che viene inclusa nel file MUI è una risorsa della versione. Se/G1 non è impostato, RC non genererà un file MUI se l'unica risorsa localizzabile inclusa nel file MUI è una risorsa della versione.

</dd> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Visualizza l'elenco delle opzioni della riga di comando.

</dd> <dt>

<span id="_I"></span><span id="_i"></span>**/I**
</dt> <dd>

Cerca nella directory specificata prima di cercare le directory specificate dalla variabile di ambiente INCLUDE.

</dd> <dt>

<span id="_j__loctype"></span><span id="_J__LOCTYPE"></span> *loctype* /j
</dt> <dd>

I tipi di risorsa localizzabili RC vengono posizionati nel linguaggio MUI (Language-dipendente). File RES. Se si imposta anche l'opzione **/q** , questa opzione viene ignorata e le informazioni nel file di configurazione RC hanno la precedenza.

**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le funzioni [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.

</dd> <dt>

<span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>sovratipo **/k** 
</dt> <dd>

Tipi di risorse sovrapposti che RC inserisce in entrambi i tipi di risorse indipendenti dalla lingua. RES e la lingua dipendente (MUI). File RES. I tipi di risorsa specificati dall'opzione **/k** devono essere un subset di quelli specificati dall'opzione **/j** . Per esempio? J2? J3? K3 specifica che RC inserisce il tipo di risorsa 3 in entrambi i file indipendenti dalla lingua e dalla lingua (MUI). Se si imposta anche l'opzione **/q** , questa opzione viene ignorata e le informazioni nel file di configurazione RC hanno la precedenza.

**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le funzioni [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.

</dd> <dt>

<span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *LangID*
</dt> <dd>

Specifica la lingua predefinita per la compilazione. Ad esempio,-L409 equivale a includere l'istruzione seguente all'inizio del file di script di risorsa: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`

Per ulteriori informazioni, vedere [identificatori di lingua](/windows/desktop/Intl/language-identifiers).

</dd> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Null termina tutte le stringhe nella tabella di stringhe.

</dd> <dt>

<span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/Q** *MUI. rcconfig*
</dt> <dd>

Un file di configurazione RC che segue il formato del file di configurazione RC. Il formato del file di configurazione RC consente ai componenti di descrivere autonomamente le informazioni sulle risorse, ad esempio il controllo delle versioni delle risorse, il percorso file MUI, i tipi di risorse e gli elementi Questo file specifica quali risorse vengono inserite nella lingua indipendente dalla lingua. File RES e quali risorse vengono inserite nel linguaggio MUI (dipendente dalla lingua). File RES. Questa opzione e le informazioni fornite nel file di configurazione RC eseguono l'override delle opzioni della riga di comando **/j** e **/k**.

**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le funzioni [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Ignorato. Fornito per la compatibilità con i makefile esistenti.

</dd> <dt>

<span id="_u"></span><span id="_U"></span>**/u**
</dt> <dd>

Definisce un simbolo per il preprocessore.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Visualizza i messaggi che segnalano lo stato di avanzamento del compilatore.

</dd> <dt>

<span id="_x"></span><span id="_X"></span>**/x**
</dt> <dd>

Impedisce a RC di controllare la variabile di ambiente INCLUDE durante la ricerca di file di intestazione o di risorse.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le opzioni non distinguono tra maiuscole e minuscole e il segno meno (-) può essere utilizzato al posto di una barra (/). È possibile combinare le opzioni di una singola lettera se non richiedono parametri aggiuntivi.

RC non genererà un file MUI nei casi seguenti.

-   Nel file RC non esistono risorse localizzabili.
-   L'unico ID lingua della risorsa specificato nel file RC è neutro (0x0).
-   Il file RC contiene risorse specificate in più di una lingua. L'eccezione è rappresentata dal caso in cui il file RC contenga due lingue e una lingua è neutra (0x0), RC genera un file MUI.

Per altre informazioni, vedere i seguenti argomenti:

-   [Definizione dei nomi per il preprocessore](defining-names-for-the-preprocessor.md)
-   [Ridenominazione del file di risorse compilato](renaming-the-compiled-resource-file.md)
-   [Ricerca di file](searching-for-files.md)
-   [Visualizzazione dei messaggi di stato](displaying-progress-messages.md)
-   [Messaggi di diagnostica RC](rc-diagnostic-messages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia utente multilingue](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 