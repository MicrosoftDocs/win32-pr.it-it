---
description: ICE53 verifica la presenza di voci nella tabella del registro di sistema che scrivono le informazioni sul programma di installazione privato o i valori dei criteri nel registro di sistema.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c323a502642e3cf5999e6cb332a434a9fc8a41db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315905"
---
# <a name="ice53"></a><span data-ttu-id="0ae2a-103">ICE53</span><span class="sxs-lookup"><span data-stu-id="0ae2a-103">ICE53</span></span>

<span data-ttu-id="0ae2a-104">ICE53 verifica la presenza di voci nella tabella del registro di sistema che scrivono le informazioni sul programma di installazione privato o i valori dei criteri nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-104">ICE53 checks for entries in the Registry table that write private installer information or policy values to the system registry.</span></span>

## <a name="result"></a><span data-ttu-id="0ae2a-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="0ae2a-105">Result</span></span>

<span data-ttu-id="0ae2a-106">ICE53 pubblica un avviso se la tabella del registro di sistema specifica la scrittura delle informazioni interne o dei criteri nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-106">ICE53 posts a warning if the Registry table specifies writing internal or policy information to the registry.</span></span>

## <a name="example"></a><span data-ttu-id="0ae2a-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="0ae2a-107">Example</span></span>

<span data-ttu-id="0ae2a-108">ICE53 invia l'avviso seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-108">ICE53 posts the following warning for the example shown.</span></span>

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

<span data-ttu-id="0ae2a-109">[Tabella del registro di sistema](registry-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="0ae2a-109">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="0ae2a-110">Registro</span><span class="sxs-lookup"><span data-stu-id="0ae2a-110">Registry</span></span>             | <span data-ttu-id="0ae2a-111">Radice</span><span class="sxs-lookup"><span data-stu-id="0ae2a-111">Root</span></span>         | <span data-ttu-id="0ae2a-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="0ae2a-112">Key</span></span>                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ae2a-113">Registry1</span><span class="sxs-lookup"><span data-stu-id="0ae2a-113">Registry1</span></span><br/> | <span data-ttu-id="0ae2a-114">1</span><span class="sxs-lookup"><span data-stu-id="0ae2a-114">1</span></span><br/> | <span data-ttu-id="0ae2a-115">**Software** \\ di **Criteri** \\ di **Microsoft** \\ **Windows** \\ **Programma di installazione** \\ **DisableRollback**</span><span class="sxs-lookup"><span data-stu-id="0ae2a-115">**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**DisableRollback**</span></span><br/> |



 

<span data-ttu-id="0ae2a-116">La riga della tabella del registro di sistema ' Registry1' scrive un valore dei criteri di sistema nel registro di sistema che influiscono sull'installazione di tutti i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0ae2a-116">Registry table row 'Registry1' writes a system policy value in the registry that affects the installation of all packages.</span></span> <span data-ttu-id="0ae2a-117">A seconda del pacchetto, può essere possibile disabilitare il rollback solo per questo pacchetto impostando la proprietà [**DisableRollback**](-disablerollback.md) nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="0ae2a-117">Depending on the package, it may be possible to disable rollback for this package alone by setting the [**DISABLEROLLBACK**](-disablerollback.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="0ae2a-118">Vedere eseguire il [rollback dell'installazione](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="0ae2a-118">See [Rollback Installation](rollback-installation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ae2a-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ae2a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ae2a-120">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="0ae2a-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




