---
description: 'Altre informazioni su: file del motore di archiviazione estendibile'
title: File del motore di archiviazione estendibile
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: c27bb0104c5923496c5dd7962ef4a9bacdc90af4
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321173"
---
# <a name="extensible-storage-engine-files"></a><span data-ttu-id="1d23f-103">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="1d23f-103">Extensible Storage Engine Files</span></span>


<span data-ttu-id="1d23f-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1d23f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-files"></a><span data-ttu-id="1d23f-105">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="1d23f-105">Extensible Storage Engine Files</span></span>

<span data-ttu-id="1d23f-106">Il motore di archiviazione estendibile utilizza i seguenti tipi di file:</span><span class="sxs-lookup"><span data-stu-id="1d23f-106">The Extensible Storage Engine uses the following types of files:</span></span>

- [<span data-ttu-id="1d23f-107">File di log delle transazioni</span><span class="sxs-lookup"><span data-stu-id="1d23f-107">Transaction Log Files</span></span>](#transaction-log-files)

- [<span data-ttu-id="1d23f-108">File di log delle transazioni temporanei</span><span class="sxs-lookup"><span data-stu-id="1d23f-108">Temporary Transaction Log Files</span></span>](#temporary-transaction-log-files)

- [<span data-ttu-id="1d23f-109">File di log delle transazioni riservati</span><span class="sxs-lookup"><span data-stu-id="1d23f-109">Reserved Transaction Log Files</span></span>](#reserved-transaction-log-files)

- [<span data-ttu-id="1d23f-110">File di checkpoint</span><span class="sxs-lookup"><span data-stu-id="1d23f-110">Checkpoint Files</span></span>](#checkpoint-files)

- [<span data-ttu-id="1d23f-111">File di database</span><span class="sxs-lookup"><span data-stu-id="1d23f-111">Database Files</span></span>](#database-files)

- [<span data-ttu-id="1d23f-112">Database temporanei</span><span class="sxs-lookup"><span data-stu-id="1d23f-112">Temporary Databases</span></span>](#temporary-databases)

- [<span data-ttu-id="1d23f-113">Scarica file mappa</span><span class="sxs-lookup"><span data-stu-id="1d23f-113">Flush Map Files</span></span>](#flush-map-files)

<span data-ttu-id="1d23f-114">Questa tabella contiene una panoramica dei nomi dei file di dati gestiti da ESE.</span><span class="sxs-lookup"><span data-stu-id="1d23f-114">This table contains an overview of the data file names that are managed by ESE.</span></span> <span data-ttu-id="1d23f-115">Per Windows Vista e versioni successive, l'impostazione JET_paramLegacyNames influisca sui nomi file utilizzati.</span><span class="sxs-lookup"><span data-stu-id="1d23f-115">For Windows Vista and later, the JET_paramLegacyNames setting impacts the file names that are used.</span></span>

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p><span data-ttu-id="1d23f-116">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="1d23f-116">Operating System</span></span></p>
    </th>
    <th>
      <p><span data-ttu-id="1d23f-117">Windows Server 2003 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="1d23f-117">Windows Server 2003 and earlier</span></span><br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p><span data-ttu-id="1d23f-118">Windows Vista e versioni successive (client)</span><span class="sxs-lookup"><span data-stu-id="1d23f-118">Windows Vista and later (client)</span></span> <br />
<span data-ttu-id="1d23f-119">Windows Server 2008 e versioni successive (Server)</span><span class="sxs-lookup"><span data-stu-id="1d23f-119">Windows Server 2008 and later (server)</span></span>
</p>
    </th>
    <th>
      <p><span data-ttu-id="1d23f-120">Aggiornamento dell'anniversario di Windows 10 e versioni successive (client)</span><span class="sxs-lookup"><span data-stu-id="1d23f-120">Windows 10 Anniversary Update and later (client)</span></span> <br />
<span data-ttu-id="1d23f-121">Windows Server 2016 e versioni successive (Server)</span><span class="sxs-lookup"><span data-stu-id="1d23f-121">Windows Server 2016 and later (server)</span></span>
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="1d23f-122">
        <strong>Impostazione JET_paramLegacyNames</strong>
      </span><span class="sxs-lookup"><span data-stu-id="1d23f-122">
        <strong>JET_paramLegacyNames setting</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-123">
        <strong>N/A</strong>
      </span><span class="sxs-lookup"><span data-stu-id="1d23f-123">
        <strong>N/A</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-124">
        <strong>Nessuna</strong>
      </span><span class="sxs-lookup"><span data-stu-id="1d23f-124">
        <strong>None</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-125">
        <strong>JET_bitESE98FileNames</strong>
      </span><span class="sxs-lookup"><span data-stu-id="1d23f-125">
        <strong>JET_bitESE98FileNames</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-126">
        <strong>Uguale a Windows Vista/Server 2008</strong>
      </span><span class="sxs-lookup"><span data-stu-id="1d23f-126">
        <strong>Same as Windows Vista/Server 2008</strong>
      </span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="1d23f-127">Log corrente</span><span class="sxs-lookup"><span data-stu-id="1d23f-127">Current Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-128">&lt;Inst &gt; . log</span><span class="sxs-lookup"><span data-stu-id="1d23f-128">&lt;inst&gt;.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-129">&lt;Inst &gt; . jtx</span><span class="sxs-lookup"><span data-stu-id="1d23f-129">&lt;inst&gt;.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-130">&lt;Inst &gt; . log</span><span class="sxs-lookup"><span data-stu-id="1d23f-130">&lt;inst&gt;.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="1d23f-131">Log pre-init</span><span class="sxs-lookup"><span data-stu-id="1d23f-131">Pre-Init Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-132">&lt;Inst &gt; tmp. log</span><span class="sxs-lookup"><span data-stu-id="1d23f-132">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-133">&lt;Inst &gt; tmp. jtx</span><span class="sxs-lookup"><span data-stu-id="1d23f-133">&lt;inst&gt;tmp.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-134">&lt;Inst &gt; tmp. log</span><span class="sxs-lookup"><span data-stu-id="1d23f-134">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="1d23f-135">Log ruotati</span><span class="sxs-lookup"><span data-stu-id="1d23f-135">Rotated Logs</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-136">&lt;Inst &gt; xxxxx. log</span><span class="sxs-lookup"><span data-stu-id="1d23f-136">&lt;inst&gt;XXXXX.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-137">&lt;Inst &gt; xxxxx. jtx dopo fffff passare a &lt; inst &gt; xxxxxxxx. jtx</span><span class="sxs-lookup"><span data-stu-id="1d23f-137">&lt;inst&gt;XXXXX.jtx after FFFFF switch to &lt;inst&gt;XXXXXXXX.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-138">&lt;Inst &gt; xxxxx. log dopo fffff passare a &lt; inst &gt; xxxxxxxx. log.</span><span class="sxs-lookup"><span data-stu-id="1d23f-138">&lt;inst&gt;XXXXX.log after FFFFF switch to &lt;inst&gt;XXXXXXXX.log.</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="1d23f-139">
        <a href="gg294069(v=exchg.10).md">File del checkpoint</a>
      </span><span class="sxs-lookup"><span data-stu-id="1d23f-139">
        <a href="gg294069(v=exchg.10).md">Checkpoint Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-140">&lt;Inst &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="1d23f-140">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-141">&lt;Inst &gt; . JCP</span><span class="sxs-lookup"><span data-stu-id="1d23f-141">&lt;inst&gt;.jcp</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-142">&lt;Inst &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="1d23f-142">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="1d23f-143">
        <a href="gg294069(v=exchg.10).md">Database temporanei</a>
      </span><span class="sxs-lookup"><span data-stu-id="1d23f-143">
        <a href="gg294069(v=exchg.10).md">Temporary Databases</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-144">&lt;nome file database temporaneo &gt; predefinito: tmp. edb</span><span class="sxs-lookup"><span data-stu-id="1d23f-144">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-145">&lt;nome file database temporaneo &gt; predefinito: tmp. edb</span><span class="sxs-lookup"><span data-stu-id="1d23f-145">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-146">&lt;nome file database temporaneo &gt; predefinito: tmp. edb</span><span class="sxs-lookup"><span data-stu-id="1d23f-146">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="1d23f-147">
        <a href="gg294069(v=exchg.10).md">File di log delle transazioni riservati</a>
      </span><span class="sxs-lookup"><span data-stu-id="1d23f-147">
        <a href="gg294069(v=exchg.10).md">Reserved Transaction Log Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-148">Res1. log &amp; Res2. log</span><span class="sxs-lookup"><span data-stu-id="1d23f-148">res1.log &amp; res2.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-149">&lt;Inst &gt; RESXXXXX. JRS</span><span class="sxs-lookup"><span data-stu-id="1d23f-149">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
    <td colspan="2">
      <p><span data-ttu-id="1d23f-150">&lt;Inst &gt; RESXXXXX. JRS</span><span class="sxs-lookup"><span data-stu-id="1d23f-150">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="1d23f-151">
        <a href="gg294069(v=exchg.10).md">File di database</a>
      </span><span class="sxs-lookup"><span data-stu-id="1d23f-151">
        <a href="gg294069(v=exchg.10).md">Database Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-152">&lt;nome file di database&gt;</span><span class="sxs-lookup"><span data-stu-id="1d23f-152">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-153">&lt;nome file di database&gt;</span><span class="sxs-lookup"><span data-stu-id="1d23f-153">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-154">&lt;nome file di database&gt;</span><span class="sxs-lookup"><span data-stu-id="1d23f-154">&lt;db file name&gt;</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="1d23f-155">
        <a href="gg294069(v=exchg.10).md">Scarica file mappa</a>
      </span><span class="sxs-lookup"><span data-stu-id="1d23f-155">
        <a href="gg294069(v=exchg.10).md">Flush Map Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-156">N/D</span><span class="sxs-lookup"><span data-stu-id="1d23f-156">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-157">N/D</span><span class="sxs-lookup"><span data-stu-id="1d23f-157">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-158">N/D</span><span class="sxs-lookup"><span data-stu-id="1d23f-158">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="1d23f-159">&lt;nome del file di database senza estensione &gt; . JFM</span><span class="sxs-lookup"><span data-stu-id="1d23f-159">&lt;db file name without extension&gt;.jfm</span></span></p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a><span data-ttu-id="1d23f-160">File di log delle transazioni</span><span class="sxs-lookup"><span data-stu-id="1d23f-160">Transaction Log Files</span></span>

<span data-ttu-id="1d23f-161">I file di log delle transazioni contengono operazioni sui file di database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-161">Transaction log files contain operations on database files.</span></span> <span data-ttu-id="1d23f-162">Contengono informazioni sufficienti per portare un database in uno stato coerente logicamente dopo una chiusura imprevista di un processo o l'arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="1d23f-162">They contain enough information to bring a database to a logically consistent state after an unexpected process termination or system shutdown.</span></span>

<span data-ttu-id="1d23f-163">I nomi dei file di log dipendono da un nome di base di tre lettere, che può essere impostato con [JET_paramBaseName](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1d23f-163">The names of the log files are dependent on a three-letter base name, which can be set with [JET_paramBaseName](./transaction-log-parameters.md).</span></span> <span data-ttu-id="1d23f-164">Negli esempi seguenti viene usato il nome di base "edb", perché questo è il nome di base predefinito.</span><span class="sxs-lookup"><span data-stu-id="1d23f-164">The examples below use a base name of "edb", because that is the default base name.</span></span> <span data-ttu-id="1d23f-165">L'estensione per i file di log delle transazioni sarà. log o. jtx a seconda che il JET_bitESE98FileNames sia impostato nel parametro JET_paramLegacyFileNames.</span><span class="sxs-lookup"><span data-stu-id="1d23f-165">The extension for the transaction log files will be either .log or .jtx depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter.</span></span> <span data-ttu-id="1d23f-166">Per ulteriori informazioni, vedere [parametri di sistema Extensible Storage Engine](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1d23f-166">For more information, see [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="1d23f-167">I file di log delle transazioni sono denominati \<base\> \<generation-number\> . log, a partire da 1.</span><span class="sxs-lookup"><span data-stu-id="1d23f-167">Transaction log files are named \<base\>\<generation-number\>.log, beginning with 1.</span></span> <span data-ttu-id="1d23f-168">Il numero di generazione del log è in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="1d23f-168">The log generation number is in hexadecimal format.</span></span> <span data-ttu-id="1d23f-169">Ad esempio, Edb00001. log è il primo log e edb000ff. log è il log di 255 io vi.</span><span class="sxs-lookup"><span data-stu-id="1d23f-169">For example, edb00001.log is the first log, and edb000ff.log is the 255th log.</span></span> <span data-ttu-id="1d23f-170">I file di log hanno cinque cifre esadecimali nel nome del file di log, fino al file di log 1048576th, a cui i file di log iniziano con il nome in formato 11,3, ad esempio edb00100000. log.</span><span class="sxs-lookup"><span data-stu-id="1d23f-170">The log files have five hexadecimal digits in the log file name, until the 1048576th log file, at which point the log files start being named in an 11.3 format (for example, edb00100000.log).</span></span> <span data-ttu-id="1d23f-171">\<base\>. log è sempre il file di log attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="1d23f-171">\<base\>.log is always the log file that is currently being used.</span></span> <span data-ttu-id="1d23f-172">Se il motore di database non è attivo, la generazione di edb. log può essere identificata usando il comando seguente: **esentutl.exe-ml edb. log**.</span><span class="sxs-lookup"><span data-stu-id="1d23f-172">If the database engine is not active, the generation of edb.log can be identified using the following command: **esentutl.exe -ml edb.log**.</span></span>

<span data-ttu-id="1d23f-173">Sebbene i file di log delle transazioni dispongano di. Estensione di LOG comunemente associata a file di testo, i file di log delle transazioni sono in formato binario e non devono mai essere modificati da un utente. Le operazioni di database vengono scritte prima nel log.</span><span class="sxs-lookup"><span data-stu-id="1d23f-173">Although transaction log files have the .LOG extension commonly associated with text files, transaction log files are in a binary format and should never be edited by a user.Database operations are written to the log first.</span></span> <span data-ttu-id="1d23f-174">I dati possono essere scritti nel file di database in un secondo momento; probabilmente immediatamente, potenzialmente molto più tardi.</span><span class="sxs-lookup"><span data-stu-id="1d23f-174">The data can be written to the database file later; possibly immediately, potentially much later.</span></span> <span data-ttu-id="1d23f-175">In caso di interruzione imprevista di un processo o di un sistema, le operazioni sono ancora presenti nei file di log e non è possibile eseguire il rollback delle transazioni incomplete.</span><span class="sxs-lookup"><span data-stu-id="1d23f-175">In the event of unexpected process or system termination, the operations are still present in the log files, and incomplete transactions can be rolled back.</span></span> <span data-ttu-id="1d23f-176">La riproduzione dei file di log delle transazioni è detta *ripristino software* e viene eseguita automaticamente quando si chiama [JetInit](./jetinit-function.md) o [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="1d23f-176">The act of replaying transaction log files is called *soft recovery*, and it is done automatically when [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md) is called.</span></span> <span data-ttu-id="1d23f-177">Il ripristino software può essere eseguito anche manualmente con l'opzione "-r" del programma Esentutl.exe.</span><span class="sxs-lookup"><span data-stu-id="1d23f-177">Soft recovery can also be performed manually with the "-r" option of the Esentutl.exe program.</span></span> <span data-ttu-id="1d23f-178">La riproduzione dei file di log delle transazioni in un database ripristinato da un backup è detta ripristino a *freddo*.</span><span class="sxs-lookup"><span data-stu-id="1d23f-178">The act of replaying transaction log files on a database that is restored from a backup is called *hard recovery*.</span></span>

<span data-ttu-id="1d23f-179">I file di log sono di dimensioni fisse, personalizzabili con [JET_paramLogFileSize](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1d23f-179">Log files are of a fixed size, customizable with [JET_paramLogFileSize](./transaction-log-parameters.md).</span></span> <span data-ttu-id="1d23f-180">Quando il file di log corrente, ovvero edb. log, viene riempito, viene rinominato in \<base\> \<generation-number\> . log e nel flusso del log delle transazioni è necessario un nuovo file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="1d23f-180">When the current log file (that is, edb.log) gets filled, it gets renamed to \<base\>\<generation-number\>.log, and a new transaction log file is needed in the transaction log stream.</span></span>

<span data-ttu-id="1d23f-181">A ogni istanza di database è associata una singola sequenza di file di log.</span><span class="sxs-lookup"><span data-stu-id="1d23f-181">Each database instance has a single log file sequence associated with it.</span></span> <span data-ttu-id="1d23f-182">In Windows XP è stato introdotto [JetCreateInstance](./jetcreateinstance-function.md), consentendo l'utilizzo di più sequenze di file di log delle transazioni da un unico processo.</span><span class="sxs-lookup"><span data-stu-id="1d23f-182">Windows XP introduced [JetCreateInstance](./jetcreateinstance-function.md), allowing multiple transaction log file sequences to be used by a single process.</span></span> <span data-ttu-id="1d23f-183">Tuttavia, nella stessa directory non possono esistere più sequenze di file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="1d23f-183">Multiple transaction log file sequences cannot exist in the same directory, however.</span></span>

<span data-ttu-id="1d23f-184">I file di log delle transazioni non dovrebbero mai essere manipolati, rinominati, spostati o eliminati manualmente perché il danneggiamento dei dati può verificarsi.</span><span class="sxs-lookup"><span data-stu-id="1d23f-184">Transaction log files should almost never be manually manipulated, renamed, moved, or deleted because data corruption can result.</span></span>

<span data-ttu-id="1d23f-185">I file di log delle transazioni verranno eliminati dal motore di database durante un backup completo (vedere [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)) o durante le normali operazioni, se è abilitata la registrazione circolare.</span><span class="sxs-lookup"><span data-stu-id="1d23f-185">Transaction log files will be deleted by the database engine during a full backup (see [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)), or during normal operations, if circular logging is enabled.</span></span>

<span data-ttu-id="1d23f-186">Al termine del riempimento di un file di log delle transazioni, il motore di database deve creare un nuovo file di log.</span><span class="sxs-lookup"><span data-stu-id="1d23f-186">After a transaction log file is filled up, the database engine needs to create a new log file.</span></span> <span data-ttu-id="1d23f-187">La registrazione circolare è un mezzo mediante il quale i file di log possono essere puliti automaticamente dal motore di database quando non sono più necessari per il ripristino dell'arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="1d23f-187">Circular logging is a means by which log files can be automatically cleaned up by the database engine when they are no longer required for crash recovery.</span></span> <span data-ttu-id="1d23f-188">Questo processo rappresenta un'alternativa alla rimozione dei file di log come prodotto dall'esecuzione di un backup.</span><span class="sxs-lookup"><span data-stu-id="1d23f-188">This process is an alternative to removing log files as a by-product of performing a backup.</span></span> <span data-ttu-id="1d23f-189">È possibile controllare la registrazione circolare con il parametro di sistema [JET_paramCircularLog](./transaction-log-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="1d23f-189">Circular logging can be controlled with the [JET_paramCircularLog](./transaction-log-parameters.md) system parameter.</span></span> <span data-ttu-id="1d23f-190">I file di log delle transazioni non devono essere eliminati utilizzando un altro metodo.</span><span class="sxs-lookup"><span data-stu-id="1d23f-190">Transaction log files should not be deleted using any other method.</span></span>

### <a name="temporary-transaction-log-files"></a><span data-ttu-id="1d23f-191">File di log delle transazioni temporanei</span><span class="sxs-lookup"><span data-stu-id="1d23f-191">Temporary Transaction Log Files</span></span>

<span data-ttu-id="1d23f-192">Quando si compila edb. log, ESE deve creare un nuovo file.</span><span class="sxs-lookup"><span data-stu-id="1d23f-192">When edb.log fills up, ESE needs to create a new file.</span></span> <span data-ttu-id="1d23f-193">Il nuovo file di transazione di log è noto come file di log delle transazioni temporaneo prima dell'utilizzo da parte di ESE.</span><span class="sxs-lookup"><span data-stu-id="1d23f-193">The new log transaction file is known as a temporary transaction log file prior to its use by ESE.</span></span>

<span data-ttu-id="1d23f-194">Quando viene creato un nuovo file di log e le relative dimensioni vengono estese, questo viene chiamato \<base\> tmp. log.</span><span class="sxs-lookup"><span data-stu-id="1d23f-194">While a new log file is created and its size extended, it will be called \<base\>tmp.log.</span></span> <span data-ttu-id="1d23f-195">La creazione di un nuovo file può essere un'operazione potenzialmente costosa, quindi ESE creerà il file di log successivo in modo proattivo come attività in background.</span><span class="sxs-lookup"><span data-stu-id="1d23f-195">Creating a new file can be a potentially costly operation, so ESE will create the next log file proactively as a background task.</span></span>

<span data-ttu-id="1d23f-196">Poiché il file di log delle transazioni temporaneo viene creato in previsione della necessità di un nuovo file di log delle transazioni, non contiene informazioni utili.</span><span class="sxs-lookup"><span data-stu-id="1d23f-196">Because the temporary transaction log file is created in anticipation of need for a new transaction log file, it does not contain any useful information.</span></span>

### <a name="reserved-transaction-log-files"></a><span data-ttu-id="1d23f-197">File di log delle transazioni riservati</span><span class="sxs-lookup"><span data-stu-id="1d23f-197">Reserved Transaction Log Files</span></span>

<span data-ttu-id="1d23f-198">I file di log delle transazioni riservati vengono creati quando il motore inizia a consentire la registrazione di operazioni importanti per ottenere una chiusura normale.</span><span class="sxs-lookup"><span data-stu-id="1d23f-198">The reserved transaction log files are created when the engine starts to allow important operations to be logged to get a clean shutdown.</span></span>

<span data-ttu-id="1d23f-199">**Windows Vista:** In Windows Vista e versioni successive, i file di log delle transazioni riservati sono denominati \<base\> RESXXXXX. JRS.</span><span class="sxs-lookup"><span data-stu-id="1d23f-199">**Windows Vista:** In Windows Vista and later, the Reserved Transaction Log Files are named \<base\>RESXXXXX.jrs.</span></span>

<span data-ttu-id="1d23f-200">**Windows Server 2003:** In Windows Server 2003 e versioni precedenti, i file di log delle transazioni riservati sono denominati Res1. log e Res2. log.</span><span class="sxs-lookup"><span data-stu-id="1d23f-200">**Windows Server 2003:** In Windows Server 2003 and earlier, The Reserved Transaction Log Files are named res1.log and res2.log.</span></span>

<span data-ttu-id="1d23f-201">Quando il motore di database esaurisce lo spazio su disco, non è possibile creare un nuovo file di log.</span><span class="sxs-lookup"><span data-stu-id="1d23f-201">When the database engine runs out of disk space it cannot create a new log file.</span></span> <span data-ttu-id="1d23f-202">L'operazione più sicura consiste nell'arrestare in modo corretto, ma è necessario che alcune operazioni, ad esempio le operazioni di rollback, siano ancora registrate.</span><span class="sxs-lookup"><span data-stu-id="1d23f-202">The safest thing to do is to shut down cleanly, but some operations (such as rollback operations) must still be logged.</span></span> <span data-ttu-id="1d23f-203">La maggior parte delle operazioni del database avrà esito negativo durante questa fase.</span><span class="sxs-lookup"><span data-stu-id="1d23f-203">Most database operations will fail during this stage.</span></span>

<span data-ttu-id="1d23f-204">Poiché i file di log delle transazioni riservati vengono creati in previsione della necessità dei file di log delle transazioni in uno scenario fuori disco, non contengono informazioni utili.</span><span class="sxs-lookup"><span data-stu-id="1d23f-204">Because the reserved transaction log files are created in anticipation of need for transaction log files in an out-of-disk scenario, they do not contain any useful information.</span></span>

### <a name="checkpoint-files"></a><span data-ttu-id="1d23f-205">file del checkpoint</span><span class="sxs-lookup"><span data-stu-id="1d23f-205">Checkpoint Files</span></span>

<span data-ttu-id="1d23f-206">Il file del checkpoint archivia il checkpoint per una particolare sequenza di file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="1d23f-206">The checkpoint file stores the checkpoint for a particular transaction log file sequence.</span></span> <span data-ttu-id="1d23f-207">Il file del checkpoint è denominato \<base\> . chk o \<base\> . JCP, a seconda che il JET_bitESE98FileNames sia impostato nel parametro JET_paramLegacyFileNames e la relativa posizione venga fornita da [JET_paramSystemPath](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1d23f-207">The checkpoint file is named \<base\>.chk or \<base\>.jcp, depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter, and its location is given by [JET_paramSystemPath](./transaction-log-parameters.md).</span></span>

<span data-ttu-id="1d23f-208">Le operazioni di database vengono innanzitutto scritte nei file di log e quindi memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="1d23f-208">Database operations are first written to the log files and then cached in memory.</span></span> <span data-ttu-id="1d23f-209">In un secondo momento, le operazioni vengono scritte nel file di database, ma per motivi di prestazioni, l'ordine in cui le operazioni vengono scritte nel file di database potrebbe non corrispondere all'ordine in cui sono state originariamente registrate.</span><span class="sxs-lookup"><span data-stu-id="1d23f-209">At some later point, the operations get written to the database file, but for performance reasons, the order in which operations are written to the database file might not match the order in which they were originally logged.</span></span> <span data-ttu-id="1d23f-210">Le operazioni scritte nel file di log delle transazioni saranno in uno dei due stati seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d23f-210">Operations written to the transaction log file will be in one of two states:</span></span>

  - <span data-ttu-id="1d23f-211">Viene scritto nel file di log delle transazioni e nel file di database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-211">Written to the transaction log file and the database file.</span></span>

  - <span data-ttu-id="1d23f-212">Viene scritto nel file di log delle transazioni e non è ancora stato scritto nel file di database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-212">Written to the transaction log file and not yet written to the database file.</span></span>

<span data-ttu-id="1d23f-213">Molte operazioni di database possono essere archiviate in un singolo file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="1d23f-213">Many database operations can be stored in a single transaction log file.</span></span> <span data-ttu-id="1d23f-214">Un file di log specificato può essere costituito dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d23f-214">A given log file can consist of the following items:</span></span>

  - <span data-ttu-id="1d23f-215">Tutte le operazioni scritte nel file di database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-215">All operations written to the database file.</span></span>

  - <span data-ttu-id="1d23f-216">Nessuna operazione scritta nel file di database</span><span class="sxs-lookup"><span data-stu-id="1d23f-216">No operations written to the database file</span></span>

  - <span data-ttu-id="1d23f-217">Una combinazione di operazioni scritte nel file di database e operazioni non ancora scritte nel file di database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-217">A mix of operations written to the database file and operations not yet written to the database file.</span></span>

<span data-ttu-id="1d23f-218">Il Checkpoint si riferisce al punto nel tempo nel flusso del log delle transazioni in cui tutte le operazioni precedenti al Checkpoint sono state scritte nel file di database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-218">The checkpoint refers to the point in time in the transaction log stream where all operations prior to the checkpoint have been written to the database file.</span></span> <span data-ttu-id="1d23f-219">Non esiste alcuna garanzia sulle operazioni che si verificano dopo il checkpoint. alcuni potrebbero essere in memoria e altri potrebbero essere scritti nel database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-219">There is no guarantee about the operations that occur after the checkpoint; some might be in memory, and some might be written to the database.</span></span>

<span data-ttu-id="1d23f-220">Poiché tutte le operazioni nei file di log prima del checkpoint sono rappresentate nel file di database, solo i file di log delle transazioni dopo il Checkpoint sono necessari per il ripristino automatico per portare un determinato database in uno stato pulito.</span><span class="sxs-lookup"><span data-stu-id="1d23f-220">Since all the operations in the log files prior to the checkpoint are represented in the database file, only the transaction log files after the checkpoint are needed for soft recovery to bring a particular database into a clean state.</span></span>

### <a name="database-files"></a><span data-ttu-id="1d23f-221">File di database</span><span class="sxs-lookup"><span data-stu-id="1d23f-221">Database Files</span></span>

<span data-ttu-id="1d23f-222">Il file di database contiene lo schema per tutte le tabelle del database, i record per tutte le tabelle nel database e gli indici sulle tabelle.</span><span class="sxs-lookup"><span data-stu-id="1d23f-222">The database file contains the schema for all of the tables in the database, the records for all of the tables in the database, and the indexes over the tables.</span></span> <span data-ttu-id="1d23f-223">Il relativo percorso viene specificato tramite [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md)o [JetAttachDatabase2](./jetattachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="1d23f-223">Its location is given using [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md), or [JetAttachDatabase2](./jetattachdatabase2-function.md).</span></span>

<span data-ttu-id="1d23f-224">Un database viene arrestato correttamente solo dopo una chiamata riuscita a [JetTerm](./jetterm-function.md) o [JetTerm2](./jetterm2-function.md).</span><span class="sxs-lookup"><span data-stu-id="1d23f-224">A database is cleanly shut down only after a successful call to [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="1d23f-225">Il programma Esentutl.exe può rilevare se un database è stato arrestato in modo corretto con l'opzione "-MH".</span><span class="sxs-lookup"><span data-stu-id="1d23f-225">The Esentutl.exe program can detect whether a database is shut down cleanly with the "-mh" option.</span></span> <span data-ttu-id="1d23f-226">Ad esempio, "esentutl.exe-MH Sample. edb" leggerà l'intestazione del database di un database denominato Sample. edb e visualizzerà lo stato di Sample. edb.</span><span class="sxs-lookup"><span data-stu-id="1d23f-226">For example, "esentutl.exe -mh sample.edb" will read the database header of a database named sample.edb, and print out the state of sample.edb.</span></span> <span data-ttu-id="1d23f-227">Potrebbe stampare "stato: arresto normale" o "stato: arresto anomalo".</span><span class="sxs-lookup"><span data-stu-id="1d23f-227">It may print out "State: Clean Shutdown" or "State: Dirty Shutdown".</span></span>

<span data-ttu-id="1d23f-228">Un database che non è stato arrestato in modo corretto è in uno stato di arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="1d23f-228">A database that has not been cleanly shut down is in a dirty shutdown state.</span></span> <span data-ttu-id="1d23f-229">Prima di Windows XP, questo stato veniva chiamato *incoerente*.</span><span class="sxs-lookup"><span data-stu-id="1d23f-229">Prior to Windows XP, this state was called *inconsistent*.</span></span> <span data-ttu-id="1d23f-230">Un database Dirty (non coerente) può essere portato a uno stato pulito con ripristino soft.</span><span class="sxs-lookup"><span data-stu-id="1d23f-230">A dirty (inconsistent) database can be brought to a clean state with soft recovery.</span></span> <span data-ttu-id="1d23f-231">Un database danneggiato non corrisponde a un database Dirty ("non coerente").</span><span class="sxs-lookup"><span data-stu-id="1d23f-231">A corrupt database is not the same as a dirty ("inconsistent") database.</span></span>

<span data-ttu-id="1d23f-232">Un database danneggiato si riferisce a un danneggiamento fisico o logico e non può essere risolto con il ripristino soft.</span><span class="sxs-lookup"><span data-stu-id="1d23f-232">A corrupt database refers to a physical or logical corruption, and cannot be fixed with soft recovery.</span></span> <span data-ttu-id="1d23f-233">I danneggiamenti fisici possono essere flip di bit, che verranno spesso intercettati dai checksum nelle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-233">Physical corruptions can be bit flips, which will frequently be caught by the checksums on the database pages.</span></span> <span data-ttu-id="1d23f-234">Un checksum non riuscito in un file di database si manifesta come errore di JET_errReadVerifyFailure.</span><span class="sxs-lookup"><span data-stu-id="1d23f-234">A failed checksum in a database file manifests itself as a JET_errReadVerifyFailure error.</span></span>

<span data-ttu-id="1d23f-235">Solo i database arrestati correttamente possono essere spostati in modo sicuro o rinominati.</span><span class="sxs-lookup"><span data-stu-id="1d23f-235">Only cleanly shut down databases can be safely moved around or renamed.</span></span> <span data-ttu-id="1d23f-236">Se un database non è stato arrestato correttamente, non può essere spostato o rinominato automaticamente in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="1d23f-236">If a database was not cleanly shut down, it cannot be automatically safely moved or renamed.</span></span>

<span data-ttu-id="1d23f-237">È possibile associare più database a una singola sequenza di file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="1d23f-237">Multiple databases can be associated with a single transaction log file sequence.</span></span>

### <a name="temporary-databases"></a><span data-ttu-id="1d23f-238">Database temporanei</span><span class="sxs-lookup"><span data-stu-id="1d23f-238">Temporary Databases</span></span>

<span data-ttu-id="1d23f-239">Il database temporaneo viene usato come archivio di backup per TempTables e viene usato anche per la creazione di indici.</span><span class="sxs-lookup"><span data-stu-id="1d23f-239">The temporary database is used as a backing store for temptables and it is also used when creating indices.</span></span>

<span data-ttu-id="1d23f-240">Il nome e il percorso sono configurati con [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1d23f-240">The name and location is configured with [JET_paramTempPath](./temporary-database-parameters.md).</span></span>

<span data-ttu-id="1d23f-241">TempTables vengono creati con [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="1d23f-241">Temptables are created with [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span> <span data-ttu-id="1d23f-242">Vengono inoltre create da alcune chiamate API e utilizzate per restituire informazioni sullo schema, ad esempio [JetGetIndexInfo](./jetgetindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="1d23f-242">They are also created by some API calls and used to return schema information (such as [JetGetIndexInfo](./jetgetindexinfo-function.md)).</span></span>

## <a name="flush-map-files"></a><span data-ttu-id="1d23f-243">Scarica file mappa</span><span class="sxs-lookup"><span data-stu-id="1d23f-243">Flush Map Files</span></span>

<span data-ttu-id="1d23f-244">A partire dall'aggiornamento dell'anniversario di Windows 10 (client) e da Windows Server 2016 (Server), ESE ha aggiunto un ulteriore livello di protezione contro le Scritture perse (o gli scaricamenti persi) 1, consentendo di rilevare tali eventi riinitialization2ti tra più processi.</span><span class="sxs-lookup"><span data-stu-id="1d23f-244">Starting with the Windows 10 Anniversary Update (client) and Windows Server 2016 (server), ESE added an additional level of protection against lost writes (or lost flushes) 1, allowing it to detect such events cross-process re-initialization2.</span></span> <span data-ttu-id="1d23f-245">Questa funzionalità richiede il salvataggio permanente dei metadati in un file separato denominato file "Flush map".</span><span class="sxs-lookup"><span data-stu-id="1d23f-245">This feature requires persisting metadata to a separate file called a "flush map" file.</span></span>

<span data-ttu-id="1d23f-246">Viene creato un file di mappa di scaricamento per ogni file di database e si trova nella stessa directory.</span><span class="sxs-lookup"><span data-stu-id="1d23f-246">One flush map file is created for each database file, and is located in the same directory.</span></span> <span data-ttu-id="1d23f-247">Il nome del file è simile a quello del file di database, ma con un'estensione diversa.</span><span class="sxs-lookup"><span data-stu-id="1d23f-247">The file is named similarly to the database file, but with a different extension.</span></span> <span data-ttu-id="1d23f-248">Ad esempio, se l'applicazione client crea un database con il percorso completo C: \\ directory \\ MyDabatase. edb, il file di mappa di scaricamento corrispondente è c: \\ directory \\ MyDabatase. JFM.</span><span class="sxs-lookup"><span data-stu-id="1d23f-248">For example, if the client application creates a database with the full path C:\\MyDirectory\\MyDabatase.edb, its corresponding flush map file is C:\\MyDirectory\\MyDabatase.jfm.</span></span>

<span data-ttu-id="1d23f-249">Questo miglioramento introduce due requisiti per la modalità di denominazione dei file di database:</span><span class="sxs-lookup"><span data-stu-id="1d23f-249">This enhancement introduces two requirements for how database files must be named:</span></span>

  - <span data-ttu-id="1d23f-250">Due database nella stessa directory non devono avere lo stesso nome di file con estensioni diverse.</span><span class="sxs-lookup"><span data-stu-id="1d23f-250">Two databases in the same directory must not have the same filename with different extensions.</span></span> <span data-ttu-id="1d23f-251">Ad esempio: C: \\ directory \\ MyDabatase. DB1 e c: \\ directory \\ MyDabatase. DB2.</span><span class="sxs-lookup"><span data-stu-id="1d23f-251">For example: C:\\MyDirectory\\MyDabatase.db1 and C:\\MyDirectory\\MyDabatase.db2.</span></span>

  - <span data-ttu-id="1d23f-252">2 \.</span><span class="sxs-lookup"><span data-stu-id="1d23f-252">2\.</span></span> <span data-ttu-id="1d23f-253">Un database non deve avere un'estensione JFM.</span><span class="sxs-lookup"><span data-stu-id="1d23f-253">A database must not have a .jfm extension.</span></span>

<span data-ttu-id="1d23f-254">Quando si copia o si sposta manualmente un file di database, anche il file di mapping di scaricamento corrispondente deve essere copiato o spostato nella stessa directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1d23f-254">When you manually copy or move a database file, its corresponding flush map file should also be, respectively, copied or moved to the same destination directory.</span></span> <span data-ttu-id="1d23f-255">Se non è presente un file di mappa di scaricamento al momento di un nuovo allegato del database (tramite [JetAttachDatabase](./jetattachdatabase-function.md), ne verrà creato uno nuovo che verrà ripopolato su richiesta man mano che le pagine vengono lette dal database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-255">If a flush map file is not present at the time of a new database attachment (via [JetAttachDatabase](./jetattachdatabase-function.md), a new one will be created and re-populated on-demand as pages are read in from the database.</span></span> <span data-ttu-id="1d23f-256">La combinazione di file di database e di mapping di scaricamento non corrispondenti viene gestita da ESE e impone l'eliminazione e la ricreazione della mappa di scaricamento non corrispondente da zero.</span><span class="sxs-lookup"><span data-stu-id="1d23f-256">Mixing mismatching database and flush map files is handled by ESE, and forces the mismatched flush map to be deleted and re-created from scratch.</span></span>

<span data-ttu-id="1d23f-257">La dimensione di un file di mappa di scaricamento è direttamente proporzionale al file di database associato e approssimativamente uguale a (tutte le dimensioni in byte, il risultato deve essere arrotondato al multiplo successivo di 8.192):</span><span class="sxs-lookup"><span data-stu-id="1d23f-257">The size of a flush map file is directly proportional to its associated database file and approximately equal to (all sizes in bytes, result must be rounded up to the next multiple of 8,192):</span></span>

`8,192 + ((<database file size> / <database page size>) / 4)`

<span data-ttu-id="1d23f-258">Ad esempio: per un database da 1,5 GB che usa una dimensione di pagina 32 KB, le dimensioni approssimative della mappa di scaricamento sono pari a 24.576 byte (o 24KB).</span><span class="sxs-lookup"><span data-stu-id="1d23f-258">For example: for a 1.5GB database using a 32KB page size, the approximate size of the flush map is 24,576 bytes (or 24KB).</span></span>

<span data-ttu-id="1d23f-259">È necessario aggiornare il file della mappa di scaricamento quando vengono scaricate le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-259">The flush map file needs to be refreshed as database pages are flushed.</span></span> <span data-ttu-id="1d23f-260">Se la registrazione transazionale è abilitata, ad esempio [JET_paramRecovery](./transaction-log-parameters.md) impostata su "on", ovvero l'impostazione predefinita, l'aggiornamento della mappa di scaricamento viene eseguito quando l'applicazione client apporta modifiche al database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-260">If transactional logging is enabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "on", the default), refreshing the flush map is performed as the client application makes modifications to the database.</span></span> <span data-ttu-id="1d23f-261">In media, l'intera mappa di scaricamento viene scritta nei supporti non volatili una volta per ogni 20% di [JET_paramCheckpointDepthMax](./database-cache-parameters.md) (in byte) dei log delle transazioni generati.</span><span class="sxs-lookup"><span data-stu-id="1d23f-261">On average, the entire flush map is written to the non-volatile media once for every 20% of [JET_paramCheckpointDepthMax](./database-cache-parameters.md) -worth (in bytes) of transactional logs generated.</span></span> <span data-ttu-id="1d23f-262">Il numero di operazioni di scrittura dipende dal modo in cui le modifiche vengono distribuite in tutto il database.</span><span class="sxs-lookup"><span data-stu-id="1d23f-262">The number of write operations depends on how distributed throughout the database the modifications are.</span></span> <span data-ttu-id="1d23f-263">Ma è al massimo approssimativamente (tutte le dimensioni in byte):</span><span class="sxs-lookup"><span data-stu-id="1d23f-263">But it is at most, approximately (all sizes in bytes):</span></span>

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

<span data-ttu-id="1d23f-264">Se la registrazione transazionale è disabilitata, ad esempio [JET_paramRecovery](./transaction-log-parameters.md) impostata su "off", la mappa di scaricamento viene aggiornata solo una volta quando il database viene scollegato in modo esplicito tramite [JetDetachDatabase](./jetdetachdatabase-function.md)o viene scollegato in modo implicito terminando la relativa istanza ESE associata (tramite una delle funzioni [JetTerm](./jetterm-function.md) , purché [JET_bitTermDirty](./jetterm2-function.md) non venga passato).</span><span class="sxs-lookup"><span data-stu-id="1d23f-264">If transactional logging is disabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "off"), the flush map gets refreshed only once when the database is explicitly detached cleanly (via [JetDetachDatabase](./jetdetachdatabase-function.md), or implicitly detached cleanly by terminating its associated ESE instance (via any of the [JetTerm](./jetterm-function.md) functions, as long as [JET_bitTermDirty](./jetterm2-function.md) is not passed).</span></span>

<span data-ttu-id="1d23f-265">1 una scrittura persa (o uno scaricamento perso) viene definita come operazione di scrittura che restituisce correttamente dal sistema operativo al motore di database ESE, ma i dati effettivi non vengono mai resi permanente nel file di database nel supporto non volatile.</span><span class="sxs-lookup"><span data-stu-id="1d23f-265">1 A lost write (or lost flush) is defined as a write operation that returns successfully from the operating system to the ESE database engine but the actual data never gets persisted to the database file in the non-volatile media.</span></span> <span data-ttu-id="1d23f-266">Il problema è in genere causato da uno stack di archiviazione (software o hardware) malfunzionante o configurato in maniera non configurata.</span><span class="sxs-lookup"><span data-stu-id="1d23f-266">It is usually caused by a malfunctioning or misconfigured storage stack (software or hardware).</span></span> <span data-ttu-id="1d23f-267">Le applicazioni client possono ricevere un errore di [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) dalle funzioni ESE che richiedono la lettura dei dati dal database se i dati si trovano in un'area che ha subito un evento di scrittura perso.</span><span class="sxs-lookup"><span data-stu-id="1d23f-267">Client applications may receive a [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) error from ESE functions that require reading data from the database if the data is located in a region that underwent a lost write event.</span></span>

<span data-ttu-id="1d23f-268">2 la possibilità di rilevare le Scritture perse entro la durata di un processo è stata apportata a partire da Windows 8 (client) e Windows Server 2012 (Server).</span><span class="sxs-lookup"><span data-stu-id="1d23f-268">2 The ability to detect lost writes within a process's lifetime has been present since Windows 8 (client) and Windows Server 2012 (server).</span></span>
